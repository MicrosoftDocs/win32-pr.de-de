---
description: Startet die Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt das Entschlüsseln eines teilweise verschlüsselten Volumes fort.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Entschlüsselungsmethode der Win32_EncryptableVolume-Klasse (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865436"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Entschlüsselungsmethode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **Entschlüsselungs** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt mit der Entschlüsselung eines vollständig verschlüsselten Volumes oder nimmt das Entschlüsseln eines teilweise verschlüsselten Volumes wieder auf.

Wenn die Entschlüsselung angehalten oder ausgeführt wird, verhält sich diese Methode genauso wie " [**resumeconversion**](resumeconversion-win32-encryptablevolume.md)". Wenn die Verschlüsselung angehalten oder in Bearbeitung ist, wird die Verschlüsselung von dieser Methode wieder hergestellt, und die Entschlüsselung wird gestartet. Nachdem die Entschlüsselung abgeschlossen ist, werden alle Schlüssel Schutzvorrichtungen auf diesem Volume aus dem System entfernt, und das Volume wird in ein Standardmäßiges NTFS-Dateisystem konvertiert.

> [!Note]  
> Wenn die Festplatte Hardware verschlüsselt ist, legt die **entschlüsselte** Methode den Bandstatus auf "immer entsperrt" fest, entfernt alle zugeordneten Metadaten und Nullen die Sicherheits-ID für das Laufwerk.

 

## <a name="syntax"></a>Syntax


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Diese Methode wird sofort zurückgegeben. Wenn das Volume bereits vollständig entschlüsselt wurde und keine anderen Fehler vorhanden sind, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**F \_ E \_ automatische Entsperrung \_ aktiviert**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Dieses Volume kann nicht entschlüsselt werden, da zum automatischen Entsperren von Datenvolumes verwendete Schlüssel verfügbar sind. <br/> Verwenden Sie [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md) , um diese Schlüssel zu entfernen.<br/> |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Durch den Aufruf der **Entschlüsselungsmethode** bleiben Daten ungeschützt.

Wenn der Schutzstatus des Volumes 1 (Schutz vor) ist, bevor diese Methode verwendet wird, wird beim erfolgreichen Abschluss dieser Methode der Schutzstatus auf 0 (Schutz deaktiviert) festgestellt, da ein teilweise verschlüsseltes Volume definitionsgemäß nicht geschützt ist.

## <a name="remarks"></a>Bemerkungen

Wenn das Volume nicht bereits vollständig entschlüsselt wurde, bewirkt das Ausführen von **entschlüsseln** , dass " [**GetConfiguration Manager Status**](getconversionstatus-win32-encryptablevolume.md) " angibt, dass die Entschlüsselung fortgesetzt wird, und zeigt den Prozentsatz des Volumes an, der verschlüsselt bleiben soll.

Wenn der Schutzstatus des Volumes "on" ist, bevor diese Methode ausgeführt wird, wird durch das Ausführen dieser Methode der Schutzstatus in "Off" geändert, da ein teilweise verschlüsseltes Volume in der Definition nicht geschützt ist.

Wenn diese Methode auf dem momentan ausgelaufenden Betriebssystem Volume ausgeführt wird und das Betriebssystem Volume zum automatischen Entsperren von Datenvolumes verwendet wird (siehe Methode [**enableautounlock**](enableautounlock-win32-encryptablevolume.md)), müssen Sie zuerst die-Methode [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md)aufrufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| Header<br/>                   | <dl> <dt>InfoCard. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
