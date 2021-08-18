---
title: IADsNameTranslate-Schnittstelle
description: Die IADsNameTranslate-Schnittstelle wird verwendet, um Distinguished Names zwischen verschiedenen Formaten zu übersetzen. Namensübersetzungen werden auf dem Verzeichnisserver ausgeführt, und diese Schnittstelle ist derzeit nur für Objekte in Active Directory verfügbar.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate-Schnittstelle ADSI
- IADsTranslate ADSI mit
- ADSI ADSI , Beispielcode C/C++ , mit IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e167363e3c35337e74851dc43126593772aac56236f27e10a98a81b533159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023448"
---
# <a name="iadsnametranslate-interface"></a>IADsNameTranslate-Schnittstelle

Die [**IADsNameTranslate-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) wird verwendet, um Distinguished Names zwischen verschiedenen Formaten zu übersetzen. Namensübersetzungen werden auf dem Verzeichnisserver ausgeführt, und diese Schnittstelle ist derzeit nur für Objekte in Active Directory verfügbar.

Im folgenden Codebeispiel wird ein Kontoname aus dem Windows in das LDAP-Format konvertiert.


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



 

 




