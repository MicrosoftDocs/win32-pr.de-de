---
description: Fordert einen TPM-Vorgang an, der physische Präsenz erfordert.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: SetPhysicalPresenceRequest-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891355"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>SetPhysicalPresenceRequest-Methode der Win32 \_ Tpm-Klasse

Die **SetPhysicalPresenceRequest-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) fordert einen TPM-Vorgang an, der physische Präsenz erfordert. Nachdem Sie diese Methode zum Übermitteln einer Anforderung verwendet haben, wenden Sie den nächsten Schritt an, der in der [**GetPhysicalPresenceTransition-Methode**](getphysicalpresencetransition-win32-tpm.md) angegeben ist. Verwenden Sie abschließend die [**GetPhysicalPresenceResponse-Methode,**](getphysicalpresenceresponse-win32-tpm.md) um zu überprüfen, ob der Vorgang erfolgreich ausgeführt wurde. Diese Methode hält BitLocker an, wenn der Aufruf der BitLocker-Wiederherstellung erforderlich sein könnte. BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.

Diese Schritte sind erforderlich, da physische Anwesenheitsvorgänge erst ausgeführt werden können, nachdem der Computer den physisch vorhandenen Benutzer erkannt hat.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ In\]
</dt> <dd>

Typ: **uint32**

Ein ganzzahliger Wert, der den angeforderten TPM-Vorgang angibt, der physische Präsenz erfordert.



| Wert                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Keine Anforderung.<br/> Verwenden Sie diesen Wert, um eine ausstehende Anforderung zu löschen.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 2 rückgängig gemacht.<br/> Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten: [**Enable**](enable-win32-tpm.md) und [**IsEnabled**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht.<br/> Weitere Informationen finden Sie in der folgenden verwandten Methode, die keine physische Präsenz umfasst: [**Deaktivieren von**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 4 rückgängig gemacht.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 3 rückgängig gemacht.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Löschen Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/> Weitere Informationen finden Sie in der folgenden verwandten Methode, die keine physische Präsenz umfasst: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Aktivieren und aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 7 rückgängig gemacht.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Deaktivieren und deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 6 rückgängig gemacht.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Ermöglicht die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 9 rückgängig gemacht.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Verhindern sie die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 8 rückgängig gemacht. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Aktivieren, Aktivieren und Zulassen der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 11 rückgängig gemacht.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Deaktivieren, Deaktivieren und Verhindern der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 10 rückgängig gemacht.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | Verzögertes physisches VorhandenseinunownedFieldUpgrade<br/> Die Einstellung für physische Präsenz wurde aktualisiert.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Löschen, Aktivieren und Aktivieren des TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird durch Vorgang 16 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/> Legt die Bereitstellung fest, die nicht physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird durch Vorgang 15 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoIELClear \_ False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 18 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNoCLEClear \_ True<br/> Legt die Bereitstellung fest, die Nicht physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 17 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNo ADRMaintenance \_ False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 20 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/> Legt die Bereitstellung fest, die Sie nicht physisch vorhanden sein müssen, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 19 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Aktivieren + Aktivieren + Löschen<br/> Aktivieren, aktivieren und löschen Sie das TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Aktivieren + Aktivieren + Deaktivieren + Aktivieren + Aktivieren<br/> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und reaktivieren Sie das TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/> Verwenden Sie die [**GetPhysicalPresenceTransition-Methode,**](getphysicalpresencetransition-win32-tpm.md) um den nächsten erforderlichen Schritt zu bestimmen.<br/>                                                  |
| <dl> <dt>**TPM \_ E \_ PPI \_ NICHT \_ UNTERSTÜTZT**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | Der Computer unterstützt keine PHYSISCHEN TPM-Anwesenheitsvorgänge mithilfe dieser Methode.<br/> Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller. Das BIOS Ihres Computers verfügt möglicherweise über alternative Unterstützung für die Konfiguration des TPM.<br/> |
| <dl> <dt>**TPM \_ E \_ \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Ein Hardwarefehler ist aufgetreten.<br/> Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Hinweise

Tpm-Vorgänge für physische Präsenz erfordern keine TPM-Besitzerautorisierung. Sie erfordern jedoch zusätzliche Schritte zum Schutz vor nicht autorisierten Änderungen am TPM.

Computer, die TPM-Vorgänge zur physischen Präsenz unterstützen, versuchen, den physisch vorhandenen Benutzer vor dem Ausführen des Vorgangs zu erkennen. Während computer sich in der Art und Weise unterscheiden können, wie diese Erkennung durchgeführt wird, besteht die Idee darin, dass ein physisch vorhandener Benutzer oder Administrator den Vorgang autorisiert.

Beispielsweise kann der Computer erfordern, dass der Benutzer den Computer neu startet. Nach dem Neustart des Computers kann der Computer ein BIOS-Bestätigungsdialogfeld anzeigen, in dem der Benutzer den Vorgang über die Tastatur bestätigen kann.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Disable**](disable-win32-tpm.md)
</dt> <dt>

[**Klar**](clear-win32-tpm.md)
</dt> </dl>

 

 
