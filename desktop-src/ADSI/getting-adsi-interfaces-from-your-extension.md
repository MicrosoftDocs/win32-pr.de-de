---
title: Erhalten von ADSI-Schnittstellen von ihrer Erweiterung
description: Eine Erweiterung muss häufig Daten aus dem Verzeichnis Objekt erhalten, an das Sie gebunden wird.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, erhalten von ADSI-Schnittstellen von ihrer Erweiterung
- ADSI ADSI, Beispielcode C/C++, erhalten von ADSI-Schnittstellen aus der Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341552"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Erhalten von ADSI-Schnittstellen von ihrer Erweiterung

Eine Erweiterung muss häufig Daten aus dem Verzeichnis Objekt erhalten, an das Sie gebunden wird. Beispielsweise kann eine Erweiterung für ein **Computer** Objekt den **dNSHostName** des aktuellen Objekts aus dem Verzeichnis erhalten. Dies kann problemlos erreicht werden, indem ein **QueryInterface** -Aufrufe für die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für den Aggregator ausgegeben werden.


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



Sie sollten die Schnittstelle sofort nach der Verwendung freigeben. Wenn die Erweiterung einen geöffneten Verweis auf den Aggregator hat, haben Sie einen Zirkel Verweis erstellt, und der Aggregator kann die Erweiterung nicht freigeben. Daher kann der Aggregator nicht freigegeben werden, und das Ergebnis sind Speicher Verluste in Ihrer Anwendung.

 

 