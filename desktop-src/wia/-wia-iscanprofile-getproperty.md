---
description: Ruft den Wert der angegebenen untergeordneten Eigenschaften in der ab. <Properties> -Element eines Scan Profils.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Iscanprofile:: GetProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345161"
---
# <a name="iscanprofilegetproperty-method"></a>Iscanprofile:: GetProperty-Methode

Ruft den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
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

Ein Zeiger auf ein Array der Identifikationsnummern der festzulegenden Eigenschaften. Jeder Wert im Array ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ out\]
</dt> <dd>

Typ: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Ein Zeiger auf ein Array von-Werten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Gibt " \_ false" zurück, wenn einer der Eigenschaftswerte nicht verfügbar ist; andernfalls wird "s \_ OK" oder ein Standard-com-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der Typ jedes Werts muss dem Typ entsprechen, der mit dem [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md)-aufrufen festgelegt wurde.

Jeder Wert im Array, auf den die *PID* zeigt, ist eine der [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md). Sie können dieses Identifikationssystem erweitern. Siehe [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).

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

 

 
