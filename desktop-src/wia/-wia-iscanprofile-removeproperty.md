---
description: Entfernt eine angegebene Liste von untergeordneten Eigenschaften im <Properties> -Element eines Scan Profils.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Iscanprofile:: RemoveProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130025"
---
# <a name="iscanprofileremoveproperty-method"></a>Iscanprofile:: RemoveProperty-Methode

Entfernt eine angegebene Liste von untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NUM* \[ in\]
</dt> <dd>

Typ: **ulong**

Die Anzahl der Einträge im Array, auf die die *PID* zeigt.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **PROPID \** _

Ein Zeiger auf ein Array von Identifikationsnummern der zu löschenden Eigenschaften. Jede ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Jeder Wert im Array, auf den die *PID* zeigt, ist eine der [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md). Sie können dieses Identifikationssystem erweitern. Siehe [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).

Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.

Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofile**](-wia-iscanprofile.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> <dt>

[WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md)
</dt> <dt>

[Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




