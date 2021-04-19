---
title: Iwmdrmlicenabmanagement processlicenabdeletionmessage-Methode (wmdrmsdk. h)
description: Mit der processlicenabdelete-Methode wird eine Lizenz gelöscht, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Processlicenabdeletionmessage-Methode Windows Media-Format
- Processlicenabdeletionmessage-Methode Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, processlicenabdeletionmessage-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373738"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>Iwmdrmlicensmanagement::P rocess licenabdeletionmessage-Methode

Mit der **processlicenabdelete** -Methode wird eine Lizenz gelöscht, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraudeletionmessage* \[ in\]
</dt> <dd>

Meldung zur Identifizierung der zu löschenden Lizenz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





