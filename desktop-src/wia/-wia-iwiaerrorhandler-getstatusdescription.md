---
description: Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Iwiaerrorhandler:: GetStatus Description-Methode (WIA. h)'
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
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368140"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Iwiaerrorhandler:: GetStatus Description-Methode

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

*punkitem* \[ in\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Zeiger auf das [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) des übertragenen Elements. Dieses Objekt implementiert mindestens [_ *IWiaItem2* *](-wia-iwiaitem2.md) und [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Typ: **HRESULT**

**HRESULT** , das der von [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangene Statuscode ist.

</dd> <dt>

*cbreslength* \[ in\]
</dt> <dd>

Type: **Long**

**Long** , d. h. die Größe der Daten, auf die von *pbData* verwiesen wird.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Zeiger auf den Datenpuffer, wie von [_ *banbeddatacallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangen.

</dd> <dt>

*pbstraudescription* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **BSTR \** _

_ *BSTR**, das eine Beschreibung des Status oder Fehlers erhält, der während der Datenübertragung aufgetreten ist. Dieser Parameter darf nicht **null** sein. Der Aufrufer muss die Zeichenfolge mit [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)freigeben, und der implemenor muss die Zeichenfolge mithilfe von " [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)" zuordnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                             | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstraudescription* enthält einen gültigen **BSTR** -Zeiger. <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *hrStatus* ist unbekannt, und es ist keine Beschreibung verfügbar. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
