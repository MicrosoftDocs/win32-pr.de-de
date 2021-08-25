---
description: Gibt den ausstehenden physischen TPM-Anwesenheitsvorgang zurück. Verwenden Sie die SetPhysicalPresenceRequest-Methode, um einen Vorgang anfordern.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: GetPhysicalPresenceRequest-Methode der Win32_Tpm Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a040f67046717660510c762109461539fd08fb337d2337db3a54d76c3e40e817
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906410"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>GetPhysicalPresenceRequest-Methode der Win32 \_ Tpm-Klasse

Die **GetPhysicalPresenceRequest-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt den ausstehenden physischen TPM-Anwesenheitsvorgang zurück. Verwenden Sie [**die SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um einen Vorgang anfordern.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein -Wert, der den ausstehenden physischen TPM-Anwesenheitsvorgang angibt.



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
<td>Keine Anforderung.<br/></td>
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
<td>Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht. <br/> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="disable-win32-tpm.md"><strong>Deaktivieren von</strong></a>.<br/></td>
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
<td>Löschen Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Löschen Sie</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Aktivieren und aktivieren Sie das TPM. <br/> Dieser Vorgang wird durch Vorgang 7 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Deaktivieren und deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 6 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Lassen Sie die Installation eines TPM-Besitzers zu. <br/> Dieser Vorgang wird durch Vorgang 9 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Verhindert die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 8 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Aktivieren, Aktivieren und Zulassen der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 11 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Deaktivieren, deaktivieren und verhindern Sie die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird durch Vorgang 10 rückgängig gemacht.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>Deferred Physical PresenceunownedFieldUpgrade<br/> Die Einstellung für die physische Präsenz wurde aktualisiert.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Löschen, Aktivieren und Aktivieren des TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM festlegen zu können.<br/> Dieser Vorgang wird durch Vorgang 16 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Legt die Bereitstellung fest, die sie nicht physisch benötigen, um das TPM festlegen zu können.<br/> Dieser Vorgang wird durch Vorgang 15 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 18 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Legt die Bereitstellung fest, die sie nicht physisch benötigen, um das TPM zu löschen.<br/> Dieser Vorgang wird durch Vorgang 17 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 20 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu verwalten.<br/> Dieser Vorgang wird durch Vorgang 19 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Aktivieren + Aktivieren + Löschen<br/> Aktivieren, aktivieren und löschen Sie das TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Aktivieren + Aktivieren + Löschen + Aktivieren + Aktivieren<br/> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und reaktivieren Sie das TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

In der folgenden Tabelle sind die allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                      | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Die Methode war erfolgreich.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ein Hardwarefehler ist aufgetreten. Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Klar**](clear-win32-tpm.md)
</dt> <dt>

[**Deaktivieren**](disable-win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
