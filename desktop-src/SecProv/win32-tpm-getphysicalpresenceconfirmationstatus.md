---
description: Gibt an, ob für einen bestimmten physischen Anwesenheitsvorgang eine Bestätigung eines physisch gegenwärtigen Benutzers erforderlich ist.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: Win32_Tpm::GetPhysicalPresenceConfirmationStatus-Methode
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
ms.openlocfilehash: 8e48fc7506b6b8ba8218d23bdeba75e960f2e3beca68c3d0a95b2aa4ea3c05e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890865"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Win32 \_ Tpm::GetPhysicalPresenceConfirmationStatus-Methode

Gibt an, ob für einen bestimmten physischen Anwesenheitsvorgang eine Bestätigung eines physisch gegenwärtigen Benutzers erforderlich ist.

Auf diese Methode kann nur von lokalen Administratoren zugegriffen werden.

## <a name="syntax"></a>Syntax


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Vorgang* \[ In\]
</dt> <dd>

Ein ganzzahliger Wert, der den angeforderten TPM-Vorgang angibt, der physisches Vorhandensein erfordert. Anbieterspezifische Befehle werden auch unterstützt.

Der *Operation-Parameter* kann aus den folgenden Werten bestehen.



| Wert                                                                                                                               | Bedeutung                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Aktivieren<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Disable<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Aktivieren<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Deaktivieren<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Löschen<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Aktivieren + Aktivieren<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Deaktivieren + Deaktivieren<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ True<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ False<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Aktivieren + Aktivieren + SetOwnerInstall \_ true<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ False + Deactivate + Disable<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | Deferred Physical PresenceunownedFieldUpgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Löschen + Aktivieren + Aktivieren<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoIGNEProvision \_ False<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoIGNEProvision \_ True<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoOMETRClear \_ False<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNoOMETRClear \_ True<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoUMAMaintenance \_ False<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoUMAMaintenance \_ True<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Aktivieren + Aktivieren + Löschen<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Aktivieren + Aktivieren + Löschen + Aktivieren + Aktivieren<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ out\]
</dt> <dd>

Gibt den Bestätigungsstatus für den Physischen Anwesenheitsbefehl zurück.

Der *ConfirmationStatus-Parameter* kann aus den folgenden Werten bestehen.



| Wert                                                                        | Bedeutung                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nicht implementiert<br/>                                             |
| <dl> <dt>1</dt> </dl> | Nur BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Blockiert für das Betriebssystem durch die BIOS-Konfiguration.<br/> |
| <dl> <dt>3</dt> </dl> | Zulässiger und physisch vorhandener Benutzer erforderlich.<br/>               |
| <dl> <dt>4</dt> </dl> | Zulässiger und physisch vorhandener Benutzer nicht erforderlich<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler und -Fehler, die für [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
