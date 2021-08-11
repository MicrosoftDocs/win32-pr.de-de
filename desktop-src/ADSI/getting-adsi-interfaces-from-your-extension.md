---
title: Abrufen von ADSI-Schnittstellen aus Ihrer Erweiterung
description: Eine Erweiterung muss häufig Daten aus dem Verzeichnisobjekt erhalten, an das sie gebunden ist.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, Abrufen von ADSI-Schnittstellen aus Ihrer Erweiterung
- ADSI ADSI , Beispielcode C/C++, Abrufen von ADSI-Schnittstellen aus Ihrer Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41df2498bd0c25996cfd0941f823e414289c0a9fbe006df846960c6f455e4301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179730"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Abrufen von ADSI-Schnittstellen aus Ihrer Erweiterung

Eine Erweiterung muss häufig Daten aus dem Verzeichnisobjekt erhalten, an das sie gebunden ist. Beispielsweise kann eine Erweiterung für ein **Computerobjekt** den **dnsHostName** des aktuellen Objekts aus dem Verzeichnis erhalten. Dies kann problemlos erreicht werden, indem ein **QueryInterface-Aufruf** für die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für den Aggregator ausgeführt wird.


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



Sie sollten die Schnittstelle sofort nach der Verwendung wieder frei geben. Wenn die Erweiterung über einen offenen Verweis auf den Aggregator verfügt, haben Sie einen Zirkelverweis erstellt, und der Aggregator kann die Erweiterung nicht frei geben. Daher kann der Aggregator nicht freigegeben werden, und das Ergebnis sind Arbeitsspeicherverlusten in Ihrer Anwendung.

 

 