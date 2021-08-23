---
description: Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte CLSID sicher aufgerufen werden kann.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: WldpIsClassInApprovedList-Funktion (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642040"
---
# <a name="wldpisclassinapprovedlist-function"></a>WldpIsClassInApprovedList-Funktion

Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte **CLSID** sicher aufgerufen werden kann. Der Funktion ist keine Importbibliothek zugeordnet. Sie müssen die Funktionen LoadLibrary und GetProcAddress verwenden, um dynamisch mit wldp.dll zu verknüpfen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Classid* 
</dt> <dd>

Die COM-Klassen-ID, die auf Genehmigung überprüft werden soll.

</dd> <dt>

*hostInformation* \[ In\]
</dt> <dd>

Eine [**\_ WLDP-HOSTINFORMATIONsstruktur, \_**](wldp-host-information.md) die den auszuwertenden Host identifiziert.

</dd> <dt>

*isApproved* \[ out\]
</dt> <dd>

Enthält nach erfolgreichem Abschluss **TRUE,** wenn die Klassen-ID genehmigt wurde. Andernfalls **FALSE**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S \_ OK** zurück, wenn erfolgreich ist, oder andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




