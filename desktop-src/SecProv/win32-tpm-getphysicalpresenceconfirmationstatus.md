---
description: Gibt an, ob für einen bestimmten physischen Anwesenheits Vorgang eine Bestätigung von einem physisch vorhandenen Benutzer erforderlich ist.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm:: getphysicalpresenceconfirmationstatus-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960122"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Win32 \_ TPM:: getphysicalpresenceconfirmationstatus-Methode

Gibt an, ob für einen bestimmten physischen Anwesenheits Vorgang eine Bestätigung von einem physisch vorhandenen Benutzer erforderlich ist.

Diese Methode ist nur für lokale Administratoren zugänglich.

## <a name="syntax"></a>Syntax


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Vorgang* \[ in\]
</dt> <dd>

Ein ganzzahliger Wert, der den angeforderten TPM-Vorgang angibt, der physisch vorhanden sein muss. Anbieterspezifische Befehle werden ebenfalls unterstützt.

Der *Vorgangs* Parameter kann aus den folgenden Werten bestehen.



| Wert                                                                                                                               | Bedeutung                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Aktivieren<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Deaktivieren<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Aktivieren<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Deaktivieren<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Clear<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Aktivieren und aktivieren<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Deaktivieren und deaktivieren<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | "Seetownerinstall" \_ true<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | "Seetownerinstall \_ false"<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Aktivieren + aktivieren + seetownerinstall \_ true<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | "Seetownerinstall \_ false + deaktivieren + deaktivieren"<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | Verzögerte physische presenceunownedfieldupgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Löschen + aktivieren + aktivieren<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | Setnoppiprovision \_ false<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | Setnoppiprovision \_ true<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | Setnoppiclear \_ false<br/>                          |
| <dl> <dt>Jahren</dt> </dl>                                                       | Setnoppiclear \_ true<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | Setnoppimaintenance \_ false<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | Setnoppimaintenance \_ true<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Aktivieren + aktivieren + löschen<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren<br/> |



 

</dd> <dt>

*Confirmationstatus* \[ vorgenommen\]
</dt> <dd>

Gibt den Bestätigungs Status für den physischen Anwesenheits Befehl zurück.

Der *confirmationstatus* -Parameter kann aus den folgenden Werten bestehen.



| Wert                                                                        | Bedeutung                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nicht implementiert<br/>                                             |
| <dl> <dt>1</dt> </dl> | Nur BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Blockiert für das Betriebssystem durch die BIOS-Konfiguration.<br/> |
| <dl> <dt>3</dt> </dl> | Der zulässige und physisch vorhandene Benutzer ist erforderlich.<br/>               |
| <dl> <dt>4</dt> </dl> | Zulässige und physisch vorhandene Benutzer nicht erforderlich<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
