---
description: Gibt die Ergebnisse eines physischen TPM-Anwesenheitsvorgangs zurück, der ausgeführt wurde.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: GetPhysicalPresenceResponse-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5f32379c9e0f538c2f9be4466b55158d0abcdd51a4d2612634b2b03ff869ed41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891860"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>GetPhysicalPresenceResponse-Methode der Win32 \_ Tpm-Klasse

Die **GetPhysicalPresenceResponse-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt die Ergebnisse eines durchgeführten physischen TPM-Anwesenheitsvorgangs zurück. Verwenden Sie die [**SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um einen Vorgang anzufordern.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein ganzzahliger Wert, der den ausgeführten PHYSISCHEN TPM-Anwesenheitsvorgang angibt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0</dt> </dl></td>
<td>Keine Anforderung.<br/> Es wurde kein physischer Anwesenheitsvorgang ausgeführt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 2 rückgängig gemacht. <br/> Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Aktivieren</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>isEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht. <br/> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz beinhaltet: <a href="disable-win32-tpm.md"><strong>Deaktivieren Sie</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>Aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 4 rückgängig gemacht.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 3 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>Löschen Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden. <br/> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Aktivieren und aktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 7 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Deaktivieren und deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 6 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Ermöglicht die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 9 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Verhindern sie die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 8 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Aktivieren, Aktivieren und Zulassen der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 11 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Deaktivieren, Deaktivieren und Verhindern der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 10 rückgängig gemacht.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>Verzögertes physisches VorhandenseinunownedFieldUpgrade<br/> Die Einstellung für physische Präsenz wurde aktualisiert.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Löschen, Aktivieren und Aktivieren des TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird durch Vorgang 16 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Legt die Bereitstellung fest, die nicht physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird durch Vorgang 15 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 18 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Legt die Bereitstellung fest, die Nicht physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 17 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 20 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 19 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Aktivieren + Aktivieren + Löschen<br/> Aktivieren, aktivieren und löschen Sie das TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Aktivieren + Aktivieren + Deaktivieren + Aktivieren + Aktivieren<br/> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und reaktivieren Sie das TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Antwort* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein ganzzahliger Wert, der die Ergebnisse der Ausführung des PHYSISCHEN TPM-Anwesenheitsvorgang angibt.

Ein physischer Anwesenheitsvorgang ist erfolgreich, wenn ein physisch vorhandener Benutzer den Vorgang bestätigt und der Vorgang fehlerfrei ausgeführt wird.

Dieser Wert kann einen TPM-Fehler enthalten. In der folgenden Tabelle sind einige der häufigsten Fehlerantworten aufgeführt.



| Wert                                                                                                                                                                                                                                                                    | Bedeutung                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                                                                                                                                                             | Der angeforderte TPM-Vorgang war erfolgreich.<br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <dt>**TPM \_ E \_ USER \_ \_ ABORT**</dt> <dt>2150171393 (0x80290301)</dt> </dl>       | Der Benutzer hat den angeforderten TPM-Vorgang abgelehnt.<br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <dt>**TPM \_ E \_ PPI \_ BIOS \_ FAILURE 2150171394**</dt> <dt>(0x80290302)</dt> </dl> | Beim Ausführen des TPM-Vorgangs ist ein BIOS-Fehler aufgetreten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                      | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Die Methode war erfolgreich.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ SAI \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ein Hardwarefehler ist aufgetreten. Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Klar**](clear-win32-tpm.md)
</dt> <dt>

[**Disable**](disable-win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> </dl>

 

 
