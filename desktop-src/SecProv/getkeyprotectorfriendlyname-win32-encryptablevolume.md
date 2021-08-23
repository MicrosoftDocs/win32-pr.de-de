---
description: Ruft den Anzeigenamen ab, mit dem eine bestimmte Schlüsselschutzvorrichtung identifiziert wird.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: GetKeyProtectorFriendlyName-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f319d555396efdf46d3511a9ca0a3088de8d4a48d032da01415c0d6fee0bcdf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892036"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorFriendlyName-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorFriendlyName-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) ruft den Anzeigenamen ab, der zum Identifizieren einer bestimmten Schlüsselschutzvorrichtung verwendet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*FriendlyName* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den benutzerspezifischen Namen enthält, der zum Identifizieren der angegebenen Schlüsselschutzvorrichtung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *VolumeKeyProtectorID-Parameter* bezieht sich nicht auf eine gültige Schlüsselschutzvorrichtung.<br/>     |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
