---
title: Referenz zum Audiokomprimierungs-Manager
description: Referenz zum Audiokomprimierungs-Manager
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows-Multimedia, ACM-Referenz
- Multimedia, ACM-Referenz
- Multimedia-Audiodatei, ACM-Referenz
- Audiodatei, ACM-Referenz)
- Audiokomprimierungs-Manager (ACM), Referenz
- ACM (Audiokomprimierungs-Manager), Referenz
- ACM-Referenz, Informationen zu
- Referenz für ACM, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516721"
---
# <a name="audio-compression-manager-reference"></a>Referenz zum Audiokomprimierungs-Manager

In diesem Abschnitt werden die Funktionen, Strukturen und Meldungen beschrieben, die dem ACM zugeordnet sind. Diese Elemente werden wie folgt gruppiert.

## <a name="drivers"></a>Treiber

-   [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmdriverclose**](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [**Acmdriverdetails**](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [**acmdriverenum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [**acmdriverenumcallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmdriverid**](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [**acmdrivermessage**](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [**acmdriveropen**](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [**acmdriverpriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmdriverproc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [**acmdriverremove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a>Filter

-   [**Acmfilterchoose**](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [**acmfilterchooabhuokproc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**Acmfilterdetails**](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [**acmfilteraufzählung**](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [**acmfilterenumcallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**Acmfiltertagdetails**](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [**acmfiltertagenum**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [**acmfiltertagenumschlag**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a>Formate

-   [**Acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [**acmformatchooabhuokproc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [**Acmformatdetails**](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [**acmformaterum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [**acmformatenumcallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmformatvorschlagen**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [**Acmformattagdetails**](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [**acmformattagenum**](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [**acmformattagenumschlag**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a>Meldungen

-   [**MM \_ ACM \_ filterchoose**](mm-acm-filterchoose.md)
-   [**MM \_ ACM \_ formatchoose**](mm-acm-formatchoose.md)

## <a name="streams"></a>Datenströme

-   [**acmstreamclose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   [**acmstreamconvertcallback**](/previous-versions//dd742925(v=vs.85))
-   [**ACMSTREAMHEADER**](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [**acmstreammessage**](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [**acmstreamopen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [**acmstreamreset**](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [**acmstreamsize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [**acmstreamunprepareheader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a>Verschiedenes

-   [**acmgetversion**](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [**acmmetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiokomprimierungs-Manager](audio-compression-manager.md)
</dt> </dl>

 

 