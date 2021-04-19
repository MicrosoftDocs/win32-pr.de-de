---
description: Fordert einen TPM-Vorgang an, der physisch vorhanden sein muss.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Setphysicalpresencerequest-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 55a0f8c5fc0a8573192f25e3901b63f24e05f7c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342837"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Setphysicalpresencerequest-Methode der Win32- \_ TPM-Klasse

Die **setphysicalpresencerequest** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse fordert einen TPM-Vorgang an, der physisch vorhanden sein muss. Nachdem Sie diese Methode zum Übermitteln einer Anforderung verwendet haben, wenden Sie den nächsten Schritt an, der in der [**getphysicalpresencetransition**](getphysicalpresencetransition-win32-tpm.md) -Methode angegeben ist. Verwenden Sie abschließend die [**getphysicalpresenceresponse**](getphysicalpresenceresponse-win32-tpm.md) -Methode, um zu überprüfen, ob der Vorgang erfolgreich ausgeführt wurde. Diese Methode hält BitLocker an, wenn durch den Aufruf von eine BitLocker-Wiederherstellung erforderlich ist. BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.

Diese Schritte sind erforderlich, da physische Anwesenheits Vorgänge nur ausgeführt werden können, nachdem der Computer den physisch vorhandenen Benutzer erkannt hat.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ in\]
</dt> <dd>

Typ: **UInt32**

Ein ganzzahliger Wert, der den angeforderten TPM-Vorgang angibt, der physisch vorhanden sein muss.



| Wert                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Keine Anforderung.<br/> Verwenden Sie diesen Wert, um eine ausstehende Anforderung zu löschen.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Aktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 2 rückgängig gemacht.<br/> Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten: [**enable**](enable-win32-tpm.md) und [**isenable**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht.<br/> Weitere Informationen finden Sie in der folgenden verwandten Methode, die keine physische Präsenz umfasst: [**Deaktivieren**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Aktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 4 rückgängig gemacht.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 3 rückgängig gemacht.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Löschen Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/> Weitere Informationen finden Sie in der folgenden verwandten Methode, die keine physische Präsenz umfasst: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Aktivieren und aktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 7 rückgängig gemacht.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Deaktivieren und deaktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 6 rückgängig gemacht.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Ermöglicht die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 9 rückgängig gemacht.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Verhindern Sie die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 8 rückgängig gemacht. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Aktivieren, aktivieren und zulassen der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 11 rückgängig gemacht.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Deaktivieren, deaktivieren und verhindern der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 10 rückgängig gemacht.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | Verzögerte physische presenceunownedfieldupgrade<br/> Die Einstellung für die physische Anwesenheit wurde aktualisiert.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Löschen, aktivieren und aktivieren Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | Setnoppiprovision \_ false<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird von Vorgang 16 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | Setnoppiprovision \_ true<br/> Legt fest, dass die Bereitstellung nicht physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird von Vorgang 15 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | Setnoppiclear \_ false<br/> Hiermit wird die Bereitstellung festgelegt, die physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch den Vorgang 18 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>           |
| <dl> <dt>Jahren</dt> </dl>                                                       | Setnoppiclear \_ true<br/> Hiermit wird die Bereitstellung festgelegt, die nicht physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird von Vorgang 17 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | Setnoppimaintenance \_ false<br/> Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.<br/> Dieser Vorgang wird durch den Vorgang 20 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | Setnoppimaintenance \_ true<br/> Legt fest, dass die Bereitstellung nicht physisch vorhanden sein muss, um das TPM beizubehalten.<br/> Dieser Vorgang wird durch den Vorgang 19 rückgängig gemacht.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Aktivieren + aktivieren + löschen<br/> Aktivieren, aktivieren und Löschen des TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren<br/> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und aktivieren Sie dann das TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Dieser Wert wird nicht unterstützt.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/> Verwenden Sie die [**getphysicalpresencetransition**](getphysicalpresencetransition-win32-tpm.md) -Methode, um den nächsten Schritt zu bestimmen, der benötigt wird.<br/>                                                  |
| <dl> <dt>**TPM \_ E- \_ ppi \_ wird 2150171395 nicht \_ unterstützt**</dt> <dt>(0x80290303)</dt> </dl> | Der Computer unterstützt keine physischen TPM-Anwesenheits Vorgänge mithilfe dieser Methode.<br/> Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller. Das BIOS des Computers kann eine Alternative Unterstützung für das Konfigurieren des TPM haben.<br/> |
| <dl> <dt>**TPM \_ E- \_ ppi- \_ ACPI- \_ Fehler**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Ein Hardwarefehler ist aufgetreten.<br/> Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Für physische Anwesenheits Vorgänge in TPM ist keine TPM-Besitzer Autorisierung erforderlich. Allerdings müssen Sie zusätzliche Schritte ausführen, um vor nicht autorisierten Änderungen am TPM zu schützen.

Computer, von denen physische TPM-Anwesenheits Vorgänge unterstützt werden, versuchen, den physisch vorhandenen Benutzer zu erkennen, bevor Sie den Vorgang ausführen. Während sich Computer in der Art der Erkennung unterscheiden können, besteht die Idee darin, dass ein physisch anwesenden Benutzer oder Administrator den Vorgang autorisiert.

Beispielsweise kann es erforderlich sein, dass der Computer vom Computer neu gestartet wird. Nachdem der Computer neu gestartet wurde, kann der Computer ein BIOS-Bestätigungs Dialogfeld anzeigen, in dem der Benutzer den Vorgang mithilfe der Tastatur bestätigen kann.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Deaktivieren**](disable-win32-tpm.md)
</dt> <dt>

[**Klartext**](clear-win32-tpm.md)
</dt> </dl>

 

 
