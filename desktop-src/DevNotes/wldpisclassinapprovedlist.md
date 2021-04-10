---
description: Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte CLSID sicher aufgerufen werden kann.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Wldpisclassinapprovedlist-Funktion (wldp. h)
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
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125857"
---
# <a name="wldpisclassinapprovedlist-function"></a>Wldpisclassinapprovedlist-Funktion

Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte **CLSID** sicher aufgerufen werden kann. Die Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die LoadLibrary-Funktion und die GetProcAddress-Funktion verwenden, um dynamisch mit wldp.dll zu verknüpfen.

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

*ClassID* 
</dt> <dd>

Die com-Klassen-ID, die auf Genehmigung überprüft werden soll.

</dd> <dt>

*Hostinformationen* \[ in\]
</dt> <dd>

Eine [**wldp- \_ Host \_ Informations**](wldp-host-information.md) Struktur, die den zu bewertenden Host identifiziert.

</dd> <dt>

*IsApproved* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss enthält **true** , wenn die Klassen-ID genehmigt ist. andernfalls **false**.

</dd> <dt>

*optionalflags* 
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




