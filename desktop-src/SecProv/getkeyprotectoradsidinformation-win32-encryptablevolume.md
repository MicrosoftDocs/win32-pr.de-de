---
description: Ruft die Sicherheits-ID und Flags ab, die zum Schützen eines Schlüssels verwendet werden.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Getkeyprotectoradsidinformation-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106367162"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a>Getkeyprotectoradsidinformation-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkeyprotectoradsidinformation** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft die Sicherheits-ID und Flags ab, die zum Schützen eines Schlüssels verwendet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet werden kann.

</dd> <dt>

*Sidstring* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Sicherheits-ID (SID) enthält.

</dd> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Flags, die das Funktionsverhalten ändern. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**F \_ DPAPI \_ ng \_ Flag \_ None**</dt> <dt>0x0000</dt> </dl>                                                                   | Keine Auswirkung.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**F \_ DPAPI \_ ng \_ Flag \_ Unlock \_ As \_ Dienst \_ Konto**</dt> <dt>0x0001</dt> </dl> | Gibt an, dass die SID-basierte Schutzvorrichtung in einem Dienst Konto geschützt wurde. Wenn dieses Flag angegeben ist, sollte der Aufrufer sicherstellen, dass er vor dem Aufrufen von [**unlockwithadsid**](unlockwithadsid-win32-encryptablevolume.md) als geeignetes Dienst Konto ausgeführt wird (z. b. durch vorübergehendes verwerfen des Identitäts Wechsels).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
