---
description: Sichert den Verschlüsselungsschlüssel des Volumes mithilfe einer Active Directory-Sicherheits-ID (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Protectkeywithadsid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357925"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Protectkeywithadsid-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **protectkeywithadsid** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe einer Sicherheits-ID (Active Directory Security Identifier, SID).

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Bezeichner für diese Schlüssel Schutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*Sidstring* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die Active Directory sid enthält, mit der der Verschlüsselungsschlüssel geschützt wird.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Flags, die das Funktionsverhalten ändern. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**F \_ DPAPI \_ ng \_ Flag \_ None**</dt> <dt>0x0000</dt> </dl>                                                                   | Keine Auswirkung.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**F \_ DPAPI \_ ng \_ Flag \_ Unlock \_ As \_ Dienst \_ Konto**</dt> <dt>0x0001</dt> </dl> | Gibt an, dass die SID-basierte Schutzvorrichtung in einem Dienst Konto geschützt wurde. Wenn dieses Flag angegeben ist, sollte der Aufrufer sicherstellen, dass er vor dem Aufrufen von [**unlockwithadsid**](unlockwithadsid-win32-encryptablevolume.md) als geeignetes Dienst Konto ausgeführt wird (z. b. durch vorübergehendes verwerfen des Identitäts Wechsels).<br/> |



 

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Ein eindeutiger Bezeichner, der der erstellten Schutzvorrichtung zugeordnet ist. Mit dieser Zeichenfolge können Sie die Schlüssel Schutzvorrichtung verwalten.

Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md) .

Standardmäßig ist es nicht möglich, ein Active Directory Konto oder eine Gruppen Schutzvorrichtung Remote hinzuzufügen. Sie müssen die eingeschränkte Delegierung auf dem Domänen Controller und dem Quellcomputer aktivieren. Führen Sie auf dem Domänen Controller die folgenden Schritte aus:

1.  Server-Manager öffnen
2.  Computer in Active Directory Rollen auswählen
3.  Ziel Client Computer auswählen und mit der rechten Maustaste klicken
4.  Registerkarte "Delegierung" auswählen
5.  Aktivieren Sie das Optionsfeld "Computer nur bei Delegierungen angegebener Dienste vertrauen".
6.  Aktivieren Sie das Optionsfeld "nur Kerberos verwenden".
7.  Klicken Sie auf "Hinzufügen".
8.  Wählen Sie "Benutzer oder Computer" aus.
9.  Host/als Dienst Prinzipal Namen auswählen

Führen Sie die Schritte 3 bis 9 auf dem Quellcomputer aus.

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

 

 
