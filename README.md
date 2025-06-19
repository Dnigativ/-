<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <title>З Днем народження!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #ffe6f0, #ccf5ff);
            font-family: 'Comic Sans MS', cursive;
            overflow-x: hidden;
        }

        .container {
            text-align: center;
            padding: 100px 20px;
            min-height: 300vh; /* сайт "довгий" */
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 4em;
            color: #ff3399;
            margin-bottom: 10px;
        }

        p {
            font-size: 1.5em;
            color: #444;
        }

        button {
            padding: 20px 40px;
            font-size: 1.5em;
            background-color: #ff66cc;
            border: none;
            color: white;
            border-radius: 12px;
            cursor: pointer;
            margin-top: 30px;
            transition: background 0.3s ease;
        }

        button:hover {
            background-color: #cc3399;
        }

        img#cake {
            margin-top: 40px;
            max-width: 300px;
        }

        /* Ромашки по краях */
        .flower {
            position: absolute;
            width: 60px;
            height: 60px;
            background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxMTEhUTExMWFhUVGB0XGBcYGRsXHxoYGhcYGBoYHxoYHSggGB0lHRYXITEhJSkrLi4uFx8zODMtNygtLisBCgoKDg0OGxAQGzAlICYyLS0zLy0tLS8wLy0tLS0tLy0tLS0tLy0vLy0vLy0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAOEA4QMBIgACEQEDEQH/xAAcAAACAgMBAQAAAAAAAAAAAAAFBgMEAAIHAQj/xABAEAACAQIEAwYEAwcCBgIDAAABAhEAAwQSITEFQVEGEyJhcYEykaGxwdHwBxQjQlJy4RUzU2JzgpKyNfEWNFT/xAAaAQABBQEAAAAAAAAAAAAAAAAEAAECAwUG/8QAMxEAAQQBBAECAggGAwAAAAAAAQACAxEEBRIhMUETUWFxFSIyM4GRocEUNFKx4fAWI9H/2gAMAwEAAhEDEQA/AOxlo9K9c6Uq8Q7cYIKQL6sY2WSYI3iuTdp/2gYpsYtzB3LgtW1GVGBysdc2ZeY5fam3jwknD9tb3LKYe/ZuPbfO1slGKyCuYTG8FT8zXL8D2gZmm+7PMeImT8zUXbHttieIMvewiJtbXYNEFtdSaCYDDPddbVtSzucqqOZNUSwiTsJw4tNhfS/Z/iFp7SnD3AbcaBTt5EcjRK9faM2bYfSgHY3ga4TDJbNtUuQDcKEsGeACZbXltRfiZ/hPGvhP2q19tYT7JN5KXMZxm5daVlR85rzD4m4s6zO8661Vw6/OpLIbnEzy1riZM2cv37ja2240e2qTBZxAKiP0aXO03ZYY0g3L91VUaIoWJO51Bk0c4XaJUnSJq1dsvygee9dfiSGaFr3DsLGlaGuIC4B2y7ODBXxbzFkdMyswAO5BEDpp03rqHYHt/hDasYV89u4iLbUQXD5QBIKgnlsaRf2pdnXsXFxDYhrvesVh/iWBMCNMo9BE85ph/YacMqX3uZVv5hDuQJtEaBZ/5g0x1Wrzwe1BdfukFTB3FIzWzppqNDzO5+9PWEdGUMpDA7Eag+43obc4fbv3GcEiDkMaAspknzj4fY1l6ngOyQ0sPIROPOIyb6KA8NsMXAECTz5Aakx8qcO7IGwP0rXD8JS38Ag9SZ+9eY3HraRmuBgFEmAW06wok/KrdOwjisO48lRyJvVdwhvHOFtiLZtligP9Gk+v9Q8qR7fY3EG2zaBgxARtCQP5vKehpu4umJvANh7xW2yfCQUaeuokacjG1G8OWa2hYQ2UZh5xrRUmNHK63BQZK5goJf7I8HRbAL2xnLMDmGo1iNfSmRk1r1BpWxNXsaGtDQqybNqnfaDSFhuxrXXuPcYohdu7AEk+IwxnYfen24sv5AfWpEH8x5UiAUlyjjHYu/F0GGRNjzcROiif0K1/Z1gLC4tReAXuwSmbTxjrOxGtdQRviuRtt+Vcp7QdnsRLX7xTKzyVQk6sSdTAqt4rlqS7QuPtEEq6tGhymdemlWbcMskb8qX+z/CVsYe1aAAhQW/uOpP1olxvjNnCWe9vOFXQDqzHQKBzNWDkcpKQcGtSdDr51cw2DRPhFeq8gMOk17dxCqhdiAo1JPKqmY0MbtzGgH3ACmZHuFEqWK9qH94X+ofOsq6woUvnv90UXC3UCprlpYmB/iqTu281PhbhuafOs6KcPNBXPiLUrNwC5dL3NFBJIFUuC498LiLd5AC9ppAbY6FSDHkTTjx/iyWLZVdXIgDp50hW3JPmaMBNKgr6T7LcTxGIsJeu20tm4MyIpLHKdmJO07xRxrciDqT8vlXNP2d9s7NvCd3irwR7XhBeNbceELGrQBHXanjs3xtMXaa/bB7vMyqWEEhdCY5az8qsBDhwkFQxHBbik5NV+XtWYThNxzBGUdfTpTUF2qOy0gkbgn8/sazHaPjF+6j8r4RQy5A3baoLhe7Eakdef+agxHE7KaPdRZ/rYLt5NRbG3VVGcnwqCx8gBJrmH7SuJYDEYBiL1t2JBslDnPeAEhSBqoIBBmN+sVpBoaKHCGJJPK53+0TjLYnGXVW6btlG/hAGVHhXMVjfWdaKdj+Afvd9LIIQEFmIA001gdZNJeEtuXGQeIa9NPenTs7xQ4bE2r0wFbxf2nQ/ryoeZw3NBUSmDjNjiuBJwdi47Wrs9yyATMarJ+DrpFdP7L4Q2cHYttOZUGadTm3MnmZolCvlfQ6Sp9RW4XWiGsDek69v3zy0qlxHiCrbZ2ViUGyiS3kOpqxeEt5Co8vIVJOouCYgX7Fu8ywXEkc1OxU+YOhoiluPSquEwqWwVQQCSx9TqTVwbUklC/hodc4kg0mdYrTjuKIhFOp1Pp+dCWaK5/U9XdA/04hZ82j8bE9Qbii+ExYaepO3lAqdvHoPh5n8KAZ5FF+G4pXWGJJHIA/hvUtM1U5DvTkFH+6bJxfS5HSmdTchV+AfU0E7X4l1tNas2muMwhmAkIPxamFs7aKMq/X/ABUN8W7KFrjBVHNj+prd7CBXLeMdrMVctiwzm3AykjwsT5nce1IPanHYi669/fe7lHhzH4fQDT33pk7YY1bmKuMk5GaVJ0OgA26aaUn8aYkiRpyPWhmv+uWpbl1rh37WbSYG2jBjiFyW2BGmWRmuT0idOtGf2m8Yb9xWzYIY4shB/YRLHy5CfOuHdnsGLl62HE286d4Jg5C0Ej8fWu8cP7I4fDX++SSoQBFY5spOggtyj7mnfNsB5Tgbktf/AIFiP/7rv/kayugfvK/12/mPzrKE9WP3Vu1y4mz1a4QhLMZ02ps4H2IRkuDEFswfKCpjQL9ZJn2HnW2H7H3ERQCJLEHyGsMT5xt5inhxHtIcVOSYOFBLWPtWLal7gXzJ3pL4piLTXZsgRHSKvdv8AbGJCMTmKhiJkQZgj5GhnZ7Ad/fSzmy5yRm3iASdOe1G1fCFKu9meD/vd1kZiqquYkaneANf1pXTMFcvYDAvZw0XGXMy59NSZaAN+ZAPOp+E9nbNgA27cMBlNzm39x2JqxilipgUEgrfC+2bYtFe1ZKJnCsbhAJUfFlCzsdJMbGrfHe0yYMLePitZgt3LqVUnKGAG8MRp0mh+Fw620CqIA6eZk/UmqfFMpQggHUH3BBH2pbk6F/tT40cTYQYbvcgJNxhmTMpEAFdGYayZEVyG6ACI0NdjtISDEZiIXNoMx0E+9LHEP2d5VVlu5zpnUiAeuUjbnoabvlMSs4DwrEYq2HS0WkanT7n5xV9+weLK6WvmRXV+zi20Q20AWDMAQNfSjPd1Q3EYObKbal3sP364VLeJQrct+HUg5lGx08qLYjiFtDBOvQVFxnFd2mnxHQfnS1dux+J86zdS1Q4zhFGLPx8I7GxfUG5x4TTYxKvMGpwtKeHvmR96acJfzKCdKt0vUjlEseKcP1TZON6VEdKX0re1bPOte+A2FbDE+VbCEQDj9qLityIifMHb6mhrQw9aaeKYYXbZB57evKlXEcMxFvdM/8AZ66bmuT1XTpTMZWCwfZauJlNa3a5eXCB+tqJdmlJzEMRJgcwfnVTAcCu3dX/AIawDHMz9qYsLgxZQKglR/KfwNXaTp0kb/VkFKGZkteNoUj2Lh/n+QAqs/DAZzGes6/epLWJR5EOsb7/AIVS4zwJMTaKlm6q0nwkGZ/xXShZqT+2nYde6e9a+JfEFG2XmB96i7I9hMNewi3cRbzXHBKyTovLT610m9aGTKdREH5RXiKqqAIAUQAKrLWh+5Lak3sJ2Jt4a0/fIrPcY7iYthjlH4+9XOKsbjGFbJbOUf0kjn5xtTQF5netL1mVKnSdNKGzcU5EWxpr9/grYXiN1kJL7kdB8hXlNH+iW+h+dZXOfQmX8Pz/AMI/+MYtV5eZqS8NgKUxxFxALEkaSYBPyEUU4RxEu2VtSdv81tw6vFJIGURfRQr8R7G7kM4n2Gw2JxLYi+GuMQqhSxVVCiNAsE6ydTzrmXAux965xJreFdlt2GLLfuIYIUgaRAeTI0Ika13jE4UssBiJ3iq/C+Hm25MypETWqhFOcL/CFs7wAY69fnUHE+HKbYUKJER58qLOla3Rr9achJDLmGFuyygZmI9yYpW4hwO/CnLOuoUyR7U8hJ1ry4OVMWAp7SRw23kZrbKVuLBgxqh2IjlINWMZhZWV+X5Vf4ngxcurdAINsFQwMSp+IEbEGPpXoiopkd4S9tralSJgT1q6CBzoXwzJkgQDOvU0Rt2QuvOppId2gw5ZAVE5TPtS49qeUiniJ0POqV/gqNqPDJ1isDU9KfO/1Yjz5BR+NlCMbXDhLNiwSRpTXg8PlUCsw3DFTUb1cAq/S9NOLbnm3H9FDKyfVoDoKAqKB4btNauYpsLbRy6KWcspUKJAG+8k6R0NH3FVTYUOWAGaIJ5xvFbBtBr3DAliTVttjVeywBgkTvVe9xJe+Wz1BJPnyH3pk6vMYANeZgRpXqHlSJ23s4zvrb4S93YVGzCfiJIgZYIO2560xNC0k1XeIWrL5XIXMAc3ISwUA9JJ096IL9DXOuwvDc1y++LvB7ruCVJBErsR5DkBoK6C9wKInloKqil3gu8KRbSD8ZxhZjbU6DePt5VTt3iCNTULt42PUk1HBnyrhMzKllnc7ceDwt6CBgjApMuDxWb1q2PShHB5n2o0Peuv0id82MHP75/RZGUwMkIC116iva9gedZWmhly65anXXfSrOGsuSuUlSTo2sbSdt6crXCLIEd2p56ia3vKqqFAAA2FYMWjODgXu4HstB+dbaAUWG4bKgtcdif+aruFtZRl+VR8OzZZJkctKuZB0reAFLPVTiGNW0ssd9AOpoS3GGJBgDSCPPr+ute9ol8aTtBjyP6igt0tmECQTr5Vyup6lO2cxxnaAtXExWOZudymnC8QVhEgN0n7DnU7WSRGw5nmfyoFwm4Q4gTy3pkN0dG+n51s6VluyYNz+xwUFlQiKSgoP3YDbegWIQqxHSi+Ma6R4YH3+dL9wEEggg860HIcLVuKCwyuROsZeZ9KuW+0r3biW0UIGaCTqYpZ4s57xRrAE+VU3vsNV3Go5aisDLzZWzbGngV/trRx8drmWe11a7iFV0UnVtAPaatu0LPSuTYHjN4XUv3iWZTtPKCIronD+M2sQp7szAGYERE8q08XNbOSOjfA+CGnx3RUiyOCJFRkg6j0oPd4ytlyjAkQDp1PKgFntFdS6zZJtsSSs6+vrRm4BDptv4+2rBHOUnYnY+U9aG4zEjOcpPhIncTz96rcPx63yLjAZ0LQOaqdo66c6KQDSu0lBcTMJqnatDOX5gQPvUXGcebMKg1YH/tjn577UBt426s+OSYmddp2+tZ+RqUML9ju0RHjPkbuCacTjXPONOVAOKY0KD/M0a84FEcHeFxZIO+3U/lUzLA0AAo1jxI0OaeCqCCDRSjY4eb+RrRSCoGWHUg7kEEaHyroXBeGCygWczn4mOs/PlQbhPGsOM796jKkhmU5spESvh56jSjvBOKLiMzICFUxJ0nSZjpQsONDFJYP1irHPe5vwVLi/CjOZJM7iqGHwlxv5T702s4JjpXlgCIoSfRMeaTebF9gK+PNkY3aqOAwwt6Hnzq/5jWvbhGxoTxzCMUlCRGuhiRWg4DGhPptuh0FQ3/sfTj35Vn/AFIdB86yk3I36NZXO/8AIH/0/r/haf0ez3/38041SuJmY9BVxzpURFdYsZRJcya8hyqxhMaLgBUNqJ1BUj1B2NVr1X8LaCrSSVPiXDBdggww2OvuIoBcwdxTBQkjSetOSVHcEj51mZmkw5L95sH4eUVDlyRCgg3DeEkHM42+GD9fWjQFbWboaROo3HTpVTi3EFsL3jqxQGGKics6SR08xRmNjR48exnSpkkdI7c5bXMSBoVal7id3vHkAqAI1ias8T7T4cWiyOHePCsESfPTQUtpiLjy1wxOuUaAfjVjioKDjliYK6kb68unnQnCWnvXBbUQzaAHTYTr00FNFpABJoz+6p3iXAokHQgciCPxrPmwGzP3380RHkOjFBI3EeB30upbgMbk5SuxgSRrEEAfKveGWcTZvMuY24IzDfNzEHpXTDalh6Gh2NwQa4hjYwfTerGafHG7c20n5L3iihGIwNwqbrkExJ6xQi9iGA0ifOnHiY/hsBudB7mKo4Pg4K+KD/U0b9QByFFlvsh7WYDgmUK7vLRMJoB6Hc+unpRVLbHbbqaXrKPhsRPe3bllp/hTmysSACJ2TcxIiB50zpiQyhgDrtOlO0+Ekt8fwWVxdmZhT5RJGk+Z+lBRh9Z+lPj2J+LUnf8AIeVU7HB7SnQTE7mdzPOsbM0l0spkY6r7R0Gb6bNpCG8GwAguZBPQxpy0FX7mCHU+5n70Q7gAQNI2qC6G5EH1/wAVq48IhjDB4Qb3l7i4oPxDBWu7ZXhA2pMhdRznnsKp9j+KW7IdXbLzB8hyjrVXthi2NoSgAVxmPMaEAj3NLtm7WVnzujna5o5H6o3Fja6MgntdE4BxwXr76wsAIDudTr61Ne4mVxO/gAykb60i8NXM45R7a+oo7ZtZWDSRBncn6GisGaSSK3+5VOQxrX01PDYhWB6VC1iRrMbxQu1jM8qvwqNSd2Y/o0bU6e1HkBwoocGlF3CdB8qysispvSb7BLcUCt8XMjMsDWTvRBL6kSpn0pVXEaxRDhbnPA0n9THWua07V5nSiObm/K08nCa1u5vhEr79T7VRxhzjKzNliMuYqI88pE+9E2wI6mqmJwDR4SJ8x+VdQspE8Fi86wBBGhr3C41LjOiMGNpsjx/K2UNB84YfOuW9pOEcats13DYjOIIyWgLZA8keQx85npTl2Cm3gsPmVg5tjvAwIbvNcxadc2aZmkCkjOOuFLgZd4g+Yk6VX/1vD4nvMPmU3ACty0SA0Ef0nUqQdxpUuJbNJoXwvg6DEXMXHja2tr2VmY/PMo/7RSSXM+D9k7mGxBGJYMyAG2AxYEH+eDvERtvPlTlbXmeXKm04Vc+cqC8Zc0ahSZyg9JqjgeAW0uXHInvHLxyEgDnvttsKjsSU+DVXtiU0jYj8/vVr9208O3SpbGKtszW1YFrcZl5rIkSPMVYCDlU0lHYeQOo0NeXV1oZxXH5GKr8Ua1SHE3kEkaDbr5/Q7dTWdkapBA/Y48/BEx4skgsBHGtZiF9z6f5rfEOFXoBVPhWOkQ3+4dTpppHyHlV5rIO4n11ouGZkzN7DYKpewsNOS7eDMS2UmfI0ZweNR2VACCFzQREAaVYuAKNfluflQZsS3fBiptgAgaamYmeUaDQVPpRRq9cAjqTAry6coJ6ClrFHublzEvcuMCBIOoRUJICKo0+Jp3J06VpxjtQroosSc2pLArpy0Ou/2quXJjiFvNKbI3PNNCabTB1BHOhWJxrW3IbxKdRyI5Eeeon3pd4J2huoxVlWD58/wq3i8YW8THXkBTR5DJW20pPjLDRUPHr63A+mhAEHnUWH7NW7hLr4VG4GxMaacqttwW44UkgBiJHMAnfpR1cGLaC2k6kATryA/Ck6Jrz9YWmDiOku2MIEXRYFSsxA2n70exuGLAIukRXuH4eqiNydyft5VJrAOAmJQLAcUtLmDsFUiTm0GnnVzB9qbd+8tqw4doOwJAHNiYgAafOkv9quGexbQ2yO7dobXWYkADmN9eUDrWn7K+L2LK3+8RxcOU5ozBl18IjRYOpkicw6UxeQ8NTgAi11fI39f0FZSt/+ar/wLn/kn51lW7mqKpWbAXQczRTg9kl8w2HvU+G4J4ZZj6eU0aw+FCCAIFc3p+jytmEk3jn8Vp5Oa1zNrF6DptI6j8q8zL1+deva6aHyoZj3vJ4lOZeYgEjz03rpullokyjqKgB8RBGh2PnVLC8Sf+dJHkIP1oj36ETI99PvStJaMm9eYZYUDzJ+tAsZj2YkBoUHTkY9fb61FYxTKZDH0P8AmsKTXYWSbQCR7o5uBI5tpmy861mq2BxfejQaj5VaGF1kkk/KtiGVsrA9hsFBvaWmiqmF4RaVzcVQLjEkv/MZ38R1jy2oiFbyNbIlY9udyfQGraUUo8QJ755YEzy0gRIHP9dKqwc3l68+f4Ub4vwrxg2UGZvjjTQbH8KEC2+vgbwmD4ToY5QOh5dflxWoYczJ3kNJBN3XutzFyGemASrnDQTcUKYPP0APl6Uz931J+32oVwfhrKS7/Fy8hH3ov3hG4mug0jGfBBT+ybWblyiSSwq2MvLaRnKsQok5RmPypcuccGIClEyruJ3+mg+tNL4gcwaUrOEC4hwUygsWAG0MTB/MdTR8m6xXSobVLziRfuLmYTpoRzGmpHUa7f4pfyHKSIn6RGuvKni5b2XkaAY3gzqf4cFeQOka9elZGp4skhDmC6RuJM1lhyBvb0Uc+Xr+vtRy1ZAAJn5E15g+FMGDORpsB1/H/NGsPhy/wiR1nSrdOx3xNO/sqvKla93CIYS2DaUkzAGtBcRx5mufwgCgGjmdSeY/X3q9xhTaw7BTqxA+Z1jppQHDWYAHShtXznwkRsNHtWYeO1/1nI7wriBMK/xf1bT7cqJu3/1Szh3nYHf8dKZLbGNV18qt0fMkna5snY8qOZC2NwrykLtT2TxWKum4z2XQKQiFnTIOohSCdNSd/lQvgmDmywQa2zlYRBnr57ct66c11uSgetJPEsGbDG4l1w119VOUjmxHw+sVoZBEY9RCsFmlP+4J0rKEwvV//I1lY/0mP6SjP4Z3uuoYUyg9Ire23I+1UsDfEtbnUeKPI/5FWb6yJrpVnqVxWjMKptxVEZUuaZgYblpG55HWprN5TqpBB5iNaZJZ3TT0FQcSw022GkxVo3lG7Co1vd5IQac3P4DnUZGhzS0+U4NG0pDb9fblUOHttJkzrpA5cvejPFOFG2C6SQNY59dKq2MBcYxljrPKeXPoa4aTTsmN5ZsJ+IC32ZcTm3dK7wJmzmIiNd/pR17xGyj3P+KoYLCG0J3bn51cGIXn4T9K63Tcd2PjtY7v/wBWNkSCSQuC0tYliTnhRyjb517dvhRI1Nel0/qX5ignHeOWsPcw6SpN68ls6jwqx+Ix5wo828qNPCoTBYQga7nU+tSWSDPy/Olrtv2st4GyTo99x/Ct9T/U3RBzPPYUJ/ZH2guYizctYhw9+2+YmACUfUGAAPiDD5daVi6Tp9YVQxeNNthmWUI3G4PSKsYq+EljtAn5xND+LX0ZFggyZEa/rekUy9xfEkyHKxzctOfuIoDfQ3DmYknrt9quJhmM6eHXXzFVcYt1LbPat94ykeCQsiRmgtpOWT7RUDz2n6Vjh+ZCSxZ5EakmPnV62xdc0QZ29DSY/b7DCw9y2/8AEC+G24IJbkOhE9DQzh37TiEud5YEzNsK23hGjTruCZHWI51EvaOykuiMgYSNqAYn9o+Cw918PdNy29rwsSmdTChpBWTz5ga0RwLuRlQyD4h768+VclXsji73FjbuKXm73r3WWEa2GDHbTaFyj7VK0l27uxicOGZSO8XMAwhlkSP7TtQW1w+4ggoZAGbLLDUawSNdfema5cIgDqPlNSBwLkcmG/mI095+lA5unR5VbiQR7IiHIdF0gmEwDmG21mD+NF1uLsTlPnVwoBQntFe7m017IXCCWAMHLzInQkdKtxMOPFZtZ+KhLM6V1uVbj7BLT3QRmVfCYzak6COcmPnS4+GaFN58154WB/Lm3VQNPU+XpS92r7U2rpQWw2UDMQygHMZ0npEbaVZ7Fi/exFthErqM0sAAOdDzv9STYBY6+CsYAG98ox/oD/03P/BvyrK6F4ug+v5VlS+jIPZR/iH+6RW4t3d03jAA3kx4elHDx+01sNbbPmAI3Gh9RppXzhx7juIxAi4/h/oXwj5c/euicV7U2cPhQ1t1dyoVFUg6wJJjYAVoh3HCHTVdx7XrjTELoAPr+vKtTfyONJDD61Q4HcBUMDIdZn1g1X41xhLN2wjMFLFipO3hI3pk6esNhiYXbm3l5UbtWwAANhQLs1xW3eVodDcX41DAkDUAkcgYP1ojjOIKqkhhESW5R+NT8JlDxHGgXLabl3ygdYBZj6AA/MVbwW7+x+9IPCeLG/xNQRlCZwinplaW9Tv8hyp7svlfXY6fl+vOqYpPUs/GlN7dtK1dXShmOxKWwGcwpMTyB8+g86KMdDQjHIt6ywBBV1MHfXkfYx8quUEM4/hLF/D3C7qECk94pByADVgR06Vwo40Pb7pVEc22za7xQXiOJz3HYHRjMToY8udXsFdEChpzxYVkYBPK3dHGuYmBGpnQcteVacG7R4jCYkYiywDgFSGEqymJVhIkaA78hRLFWLiAZrbrmkLKkZiI0EjU6j50/dlv2S281xsdluSF7tUZ0jfNm+Ek7CPKo45cSbUpGgdJh7C9rRxW1cDqLbpo6q06aFWEjRTqNZ1Bo7h+DoqGCcxMz6bCKH8B7EYbA3jew2dAy5HQsXVhMg+LUEHz5mmTLpRVKpQqkACqzbQNhzqe7iFHMTsB59K0YADyFRseEqXLO1vZCxh8OvdJduX3uAAiWJmSxKqIAAHTmNam7BdiBeuXTjLLZcgyBpXxEnMYBB0AHzroYsljMGiXD8NAkiD+FV+kC60lT4RwgYdCgYsBCqTuE5LPOBpPkKIxG3oKpcV4lkIVRJIk+XT1qlb4oxeTEbQOUkSfOg5tUxoZPTcef7IhmLI9u4DhFyvua0uptHL79anssCJGorYoa0RThYQ/Shx2JBTXQ6b9dD9IpL7W4jHXkZLWQWQviYnxPO+gGw899accSwHxEAedUsZhlupkDEA7lYHtqNqZwvhJcZwvALtwFjcUEb6En7inDsRwC8t1Ws4lgV1aQMsbEFd2B6SPUVNf4LcsXRkm4twkQBBX11jznyNUcfZxNrE2rVj47zZYkgZdZYkbAAEn0oX0Q02n4XXtetZUHcjy+v517RNn2SXzE/Z+6mt1IBWd5I10nodDpVROHZrqWlUlrjBEjmWIA+pFd04u7d0iXXQ35JJTLOXUaZtNdPrFV+H9j7aX8NeEh7ZJdZ8JJQwY5EGKz8d0kj+eknt29JR7TdncZw7AhkxAdLZytCkFVYiGDE8m08gaRuP8G4gES9ibV4qyyrMM2UM2gaP9skkaNB1HpX0ti7KspVgCDuDqNDP3FZatyJP6860gylFfJrd4hZfEk+Fhqs/8rDn6GjnDO0d9TYW7duXLNlpFstIAiPUwDoDMcorqfb3sJd4hjkZCtq0toB7hElmzMYVR8RAjUkDXntSN+0DsF/py27iX+8S4+QKywwIUsTIMEadOYpjdJ07YG8gu2cQkNBDAjmpEET6E0x8e4/aICIWJYzMEQBrz84+Vco/Z5xaGGGZSQSWUj+XSSD5fnTd2nxyWEW6QSAcunU7fUVWBtBpK7TDhf2kYUgozEXVlSCAoJHMEn6VxTGC7ev3MNhHuPavvItKzBXb4iShIUwQTJ6VU4irGLj/zkt8z/miHB+E4hGt3rKXs6MHVltuRI9tRy8waYS2LKjaYLH7IsU1ks162t2SBbglYG3jHX+3nVXsr2KvnGixfUoLUXXJ8QZQwgKdmDHTy15iK7J2e4ob9oPctXLT7Ojqy69RmGoq5ftAHNptE+9WEAi06Xu2fAxjMMbU5XzKVf+iCMzD/ALSw96M8Pa8iIuR7uUBc5KhiNszFiAeprc31B3BIjQH3q3/qiTENPQa/apAg9J1dtu3MD2NBePYsgi2mZTuT5a6AijdtJ3+VBO0eHhlcA7EHfTp+NA6o6RuM4x9/t5V+MGmUbkDYifPefxminCr7E5TBgSC0k79JoUVEzRjguEOrkb7enWuc0j1TkDZdeVp5wjEfx8IthmKkzrPtHpV/l+FULZafC0noRVy0fOY3PnXZLFSpjh/Fuac/yqtZQ8+tNGO4WLhDbMdz7V5huEKhzHWK5KbRch87qraTd/P4LWjzY2xj3CmwVpggBPKtcQlz+Uj5fjV0iNtRUJxSTlJg9D+ta6pkYYwNHjhZRNm0H7oswDDXqa9TAutwsLzlCI7shYB6ggBvYk0TusOVA+K8bS2HEywHwjUydqi97YxbinDS7pW3AAoBxHgPeYu1ie9dGsCECZdyTmJzAzIMRFUcLx+45AIjnPr60Xw2MJ8IgseZ29agJ2P4CkYnDtXc1z/iXP8Azb86yqvcXf8Aij5VlXWVXSsYXs3btz8R1nUyAYiY5nzoqqfCx3B1+01dtkHaqnE8SLa+Z0jrUXGOBhceAE4BcaCnujQ1IiADyFLX+pPpPkY9NR+FF8BxIPo2/IDnQOPq+PO/YDR8X5V8mJJG3cQroTcnSgvFuB4fFOrX7K3QgIQPJAmJOWYkwNfIUde3O+3StWtiIrT7Qy4XZ7OPheJ3XW2ww2ZlS4QFUZwGCgTOUGVDbHKOtF+3OFBwpUjUMm/9wmui8XtoEbSVynMPLbn6ilbH8OtXFZCWZAylepGmYEwNIERWZl5rMd2xytZC54sLmeE48uDxdi61vOiZsyjeCuWROkiZ1+m9ds4Vxu1fRXth/EJCshVvkaT8JwDCWwLn7v31zPlBdsxtiTDZdAdNtD6098LFsL/DDRzMQSfMnWr8OQPjG1VuYW8FWVB5rHuKWOMOWusJ8I0jWNpn9dKb1XyjzOtBeL8MLNmTeNR18/WqdVhlkgqPv29wiMR7GyW9LAA3XcfQg/hTb2fdWGY7x9edAG4bdIIVYMxJOnmdNxTDw5DZUA6wI6T+VA6PBOxxLwQ34+6IzXxuA29oxm9qjChieg+9aWnLDMfYdBUuF+H1k/WugWcqxwSZ5yiY6df/AKFbZMum3T8q2uPDT10/Xyre8BFMGgdJ7URb2Na3GyqiqQMzayeWrEDqTHyk8qWMV2haxfe0650BBU7MAQDHQxNIPaniN+5dW7ZZlYXQwVWZRA3Bg7Eb9ZNRLglS7lcaCvr96lagvDOMJiLaPKq7CSmYEqRuPt86u2saG/7TBH2PyqYTKYuV8x0qC+VzKY1HltQTD9rLFzG3cCrEXbag66BpEsF6kAqT6+RozcuqBqdQKRSQzj3ERatsc2uywdczaD6mleykiWMk7k6z7/SmzF4fv0ZRoG5xrPUUruptsyOIjTyPQz+tq5vXGyHaR9n91p4DmC77VPFYEOvhMc9Dvzor2ewxyA5dTz0GnpyqvblyUtjMwAkbQDMEn2NMvD8NlQCNtwdwajozZHOJd9nwpZz2dNWndn+k/MfnWVbgf0n9e9ZXR0stXlnmo9jQTjqkOJ6abn139qZkFUeKYUXVgHbY+fT0oTU8Z2RjuYzvv8ldjSCOQOKUiDI6c6ucOJ7xcu8/r6V7c4ZdBjLOsco+tFeFcKKGX35eX+a5bC03IdO3c0gA3fyWrPlx+maN2i2Uxyqvdssf5vlpVkkjzqji+Kd2yqyNDbNpE9N9K7Vzg0WViAE9Khj8NAOxJEeLaDuvlJg+oFLjJB1Hi+H/AB50zYjF5mkA1GwtkDNAzA76fCJ99iaxNR0715A8GkTDNsFUgZtuFK6LpmKMAC0GS6tzIBAI8vOj3CMUGQQNV0j8aojiCXkzZPCDKEiDPMwdhvVKScxXQc60MSIws2qqR242mNsaCwUHM3lsK3G3maA8JvKhcuQumhOmmpNWuC8btYq131ozbzMoJ0nKYLehiR5RRgNhVIhYYEsOh+4Fe3I2PtQexjYul/5WMH05Vf4ti0S2HY6SIjXekCkh3GsTdsrnVvAsyhgA6aaxIrbs/wBpDesKxABVir68hrMctCPlQDi/FXuDuyQUJ1ManmAaAvbKMSs66ECqSTvsdKfFUulYvHq6C4jQgGbMdNB16c6A8V7b2Wssthz3sgTlMCCJMsIIIml2y1woyFmFszCbbxO28nWg3EUKqVy67AjmKrlnLfCTW2vL/FhqSSzczvPvXmCxQeTVO3ZAArLi5fEunWs8ZZLkWYPq2jVzEskMk5l2jQk0Gscf4rhXuYgsrhypdX8XhQMAunwiG1I1kA+pjDqSAaCdqONd2ptBTmYRJGgHl1NacbzSDcEN7J9pnsY98ZdTvWuh8wnLBchpUkGIiI6aV0DBdt7mPxVrC2LXdK5l7hOZgigs0CIUwInXU1yK0CDrRPgHGL+ExC4iyoLKCMraghhqDGo5HTpTeob7UF9NIoUaegqs9tWYKQCN/lSh2h/aBZt4NLtl1a/eACJuVOzFl3AXXfcxTXhzDJ6R9Kv4PCe1IthVbQAZtPcbVO1r2PWvbyg6HntUF7GLbjvGCgmAx2noTy2pUGhPyVvlb9Cvaz97t/8AET/yH51lLcEqKlLsdzAre0ZPkNqUexXHbuNF25dyqFcKttdlGWZJOrEzv5aAU1LcBlRy38vKpA2LTKS62gPnNWNxVG5dBbL0H3qXDXo8J9qdJSd5GjfOtL6qymYIrzE3gCAedCbNzNmYKVkkEehifeKiT4The+9exUmSob9sgEqATyBMA+8aVHoJKpjMOoyhYA5gVBiG8JA6UFuceuG7lu2xbA0gEmD5kiiaNm22qmOZkl7CpuY5vapW8CqoykkgzMmd/XlVLgmBWzaNtBCyxA6ZiSaNX8MW2MVQxd/uCFKk5pIp5Htjbud0ma0uNBT2LvhGbf8AWtR3VZlIO06ela8Pxq3DB0OmnU9BVziFi7kItKM8aZpAH/MYE0o5GyC2m0nNLTRCW8aseGdRrVLh/ElZ2UjUaf5qLH8ExlnPfuXrbCIYAEaddaDcFLd6GAEQZ1pnPAcAoXynFnWpeA8Mt4rEMjEgW1UsNQYZplSCIPhAnkCaAcP4lcu3GTu8oUxJMzTBw/HPhbneIocMAtwaBiATDAkxpJ0PLaozt3N4U2nlMmK4NZwqKLULo4OYBzcYlSAwP+5u3sTtST2r7P3Lbi5bUd1cbTLMKYkqQdtjG9O+MxGe8juoC2pzMZ/mAy+EbrMrM7jzpft8QuC0bLQ6ER4pJHSDM6ec0EyDeSSKHj8lf6m0cITaUADShvavCG5hzkUEp4pPQdKKYy22XwmCOdCeK41+7ZAZzCNqPaABSHPK5omIObMaI4O/mMKdOlDsVYKmo7TkEEb0nMDhwoo3dtEKxXeJru3Ce0ljFWZsXAbiquYAGUZhOs9IPyrlXZ3CG8v8NVLwrSymBrqNYGonnyHtHwngjXcYq4Z3tBh/FZCVygHWCIkERB2kzQ8E1OLSE9FdV49xhzbDKcptkePTV5A0HpM+tUOKcdfEWxbZFGxJ8xOoHKt8Rk761g7cRbUu4GsKBCg+ZLT7Vcw/A06k69ary48iQ1G7giiETA+NvLglfuR+jWU3f6On9IrKA+iZv6giP41vsucdgf8A5C3/AGv/AOjV1/gmx9vxrysroovsBZp7Xtj/AHn9/vUmJ+Jf10rKypJLS/8AEff715b+I+lZWVHynUiVqaysp0kl9pv9256D/wBRRTh3wD0rKysXC/mJfn+5Rk/3bPkr9qlztX8Y/t/E1lZROpfy5/D+6hifehVOBf79j/qr/wCwrpVz4z/Z+NZWVTpH3bvmp5v2x8ki9sv/ANZ/1yNIvA/hPr+FeVlFyfeBB+US4J/uv6mi2J2rKyrm9JJi7SfGv/SH/vQOsrKYdKS0xHwn0oBiNj6VlZTOTJF4hzoSu9ZWU0P2VAJ07J/7yf8ARufY05dhN73pa/8AQ1lZQzfvW/ipBTdj/wD5HG/2/iKd7HP1/KsrKMZ5+ZTN6VmsrKyrE6//2Q==');/* ромашка */
            background-size: cover;
            opacity: 0.7;
            animation: float 10s infinite linear;
        }

        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            100% {
                transform: translateY(-3000px) rotate(360deg);
            }
        }

        /* Генерація кількох ромашок */
        .flower:nth-child(even) { animation-duration: 12s; }
        .flower:nth-child(odd) { animation-duration: 15s; }

    </style>
</head>
<body>
<!-- Ромашки по краях -->
<script>
    for (let i = 0; i < 400; i++) {
        const flower = document.createElement('div');
        flower.className = 'flower';
        flower.style.left = Math.random() * window.innerWidth + 'px';
        flower.style.top = (Math.random() * 2000 + 1000) + 'px'; // щоб вилітали знизу
        document.body.appendChild(flower);
    }
</script>
<button onclick="playVideo()">WW</button>

<div id="videoContainer" style="display:none; margin-top: 20px;">
    <iframe
            id="ytplayer"
            width="1"
            height="1"
            src=""
            frameborder="0"
            allow="autoplay; encrypted-media"
            allowfullscreen
    ></iframe>
</div>


<script>
    function playVideo() {
        const video = document.getElementById("ytplayer");
        const container = document.getElementById("videoContainer");

        video.src = "https://www.youtube.com/embed/rFvV5_UnSeM?start=73&autoplay=1";
        container.style.display = "block";
    }
</script>

<div class="container">
    <h1>🎉 З Днем народження! 🎂</h1>
    <center>
    <p>У цей особливий день хочеться побажати тобі безмежного щастя, глибокої радості та щирих усмішок щодня! Нехай твоє життя буде схоже на яскраву мозаїку, де кожен фрагмент — це щасливий спогад, натхнення, любов і здійснена мрія.

        Бажаю, щоб у твоєму серці завжди панував спокій, а навколо тебе — добрі, щирі та вірні люди. Щоб здоров’я було міцним, як сталь, а душа — легкою, мов весняний вітер. Нехай усі труднощі будуть тимчасовими, а кожна нова вершина — лише черговим підтвердженням твоєї сили та таланту.

        Хай твій дім буде сповнений тепла, затишку та любові. Хай удача супроводжує тебе в усьому, а натхнення ніколи не залишає. Бажаю, щоб кожен день приносив радість, щоб життя дарувало якомога більше приводів для щасливих миттєвостей!

        Нехай усе задумане здійсниться, а нові мрії з’являються щодня — ще красивіші, ще сміливіші. Бажаю тобі світла в серці, гармонії в душі, стабільності у справах і чудес в житті.

        Зі святом тебе! Будь щасливий/щаслива сьогодні й завжди! 💖🎂🎈</p></center>



    <!-- Встав свій mp3-файл сюди -->


    <img id="cake" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS3Y2jGOFm2IXwlzLW1Wch-YTfluMbjiFQVQA&s" alt="святковий торт">
</div>

<script>
    function playSong() {
        const audio = document.getElementById("song");
        audio.play();
    }
</script>
</body>
</html>
