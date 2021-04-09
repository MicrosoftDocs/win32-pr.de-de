---
title: Abrufen eines Benutzers (SDO)
description: Abrufen eines Benutzers (SDO)
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948920"
---
# <a name="retrieving-a-user-sdo"></a>Abrufen eines Benutzers (SDO)

Mit dem folgenden Code wird ein Server Datenobjekt (SDO) für den Administrator abgerufen.


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**Isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**Isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[**Isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 