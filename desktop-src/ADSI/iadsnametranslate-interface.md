---
title: Iadsnametranslation-Schnittstelle
description: Die iadsnametranslation-Schnittstelle wird verwendet, um Distinguished Names zwischen verschiedenen Formaten zu übersetzen. Namens Übersetzungen werden auf dem Verzeichnisserver ausgeführt, und diese Schnittstelle ist derzeit nur für Objekte in Active Directory verfügbar.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Iadsnametranslation-Schnittstelle ADSI
- Iadstranslate ADSI, using
- ADSI ADSI, Beispielcode C/C++, using iadstranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855296"
---
# <a name="iadsnametranslate-interface"></a>Iadsnametranslation-Schnittstelle

Die [**iadsnametranslation**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) -Schnittstelle wird verwendet, um Distinguished Names zwischen verschiedenen Formaten zu übersetzen. Namens Übersetzungen werden auf dem Verzeichnisserver ausgeführt, und diese Schnittstelle ist derzeit nur für Objekte in Active Directory verfügbar.

Im folgenden Codebeispiel wird ein Konto Name aus dem Windows-Format in das LDAP-Format konvertiert.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




