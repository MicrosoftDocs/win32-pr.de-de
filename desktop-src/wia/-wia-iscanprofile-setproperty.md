---
description: Legt den Wert der angegebenen untergeordneten Eigenschaften im <Properties> -Element eines Scan Profils.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Iscanprofile:: SetProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752856"
---
# <a name="iscanprofilesetproperty-method"></a>Iscanprofile:: SetProperty-Methode

Legt den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NUM* \[ in\]
</dt> <dd>

Typ: **ulong**

Die Anzahl der Einträge in den Arrays, auf die von *PID* und *pvar* verwiesen wird.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **PROPID \** _

Ein Zeiger auf ein Array von Identifikationsnummern der festzulegenden Eigenschaften. Jeder Wert im Array ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ in\]
</dt> <dd>

Typ: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Ein Zeiger auf ein Array von Werten, die den Eigenschaften zugewiesen werden sollen.

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

 

 
