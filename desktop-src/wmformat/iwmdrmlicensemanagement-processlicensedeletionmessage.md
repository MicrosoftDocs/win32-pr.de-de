---
title: IWMDRMLicenseManagement ProcessLicenseDeletionMessage-Methode (Wmdrmsdk.h)
description: Die ProcessLicenseDeletion-Methode löscht eine Lizenz, die für Inhalte importiert wurde, die ursprünglich mit einem anderen Inhaltsschutzsystem geschützt wurden.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- ProcessLicenseDeletionMessage-Methode windows Media Format
- ProcessLicenseDeletionMessage-Methode windows Media Format , IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , ProcessLicenseDeletionMessage-Methode
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
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027588"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement::P rocessLicenseDeletionMessage-Methode

Die **ProcessLicenseDeletion-Methode** löscht eine Lizenz, die für Inhalte importiert wurde, die ursprünglich mit einem anderen Inhaltsschutzsystem geschützt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDeletionMessage* \[ In\]
</dt> <dd>

Meldung, die die zu löschende Lizenz identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





