---
description: Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: IWiaErrorHandler::GetStatusDescription-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208302"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>IWiaErrorHandler::GetStatusDescription-Methode

Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*-Item* \[ In\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Zeiger auf die [IUnknown des](/windows/win32/api/unknwn/nn-unknwn-iunknown) zu übertragenden Elements. Dieses Objekt implementiert [**IWiaItem2**](-wia-iwiaitem2.md) und [**IWiaDataTransfer minimal.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)

</dd> <dt>

*hrStatus* \[ In\]
</dt> <dd>

Typ: **HRESULT**

**HRESULT,** bei dem es sich um den Statuscode handelt, der von [**BandedDataCallback empfangen wird.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ In\]
</dt> <dd>

Typ: **LONG**

**LONG,** das die Größe der Daten ist, auf die von *pbData verwiesen wird.*

</dd> <dt>

*pbData* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Zeiger auf den Datenpuffer, der von [**BandedDataCallback empfangen wird.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*pbstrDescription* \[ out\]
</dt> <dd>

Typ: **BSTR \***

**BSTR,** der eine Beschreibung des Status oder Fehlers empfängt, der während der Datenübertragung aufgetreten ist. Dieser Parameter darf nicht **NULL sein.** Der Aufrufer muss die Zeichenfolge mit [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)frei geben, und der Implementor muss die Zeichenfolge mit [SysAllocString zuordnen.](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                             | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstrDescription enthält* einen gültigen **BSTR-Zeiger.** <br/>  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *hrStatus* ist unbekannt, und es ist keine Beschreibung verfügbar. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
