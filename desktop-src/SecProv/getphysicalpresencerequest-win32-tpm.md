---
description: Gibt die physische Anwesenheits Operation für das TPM zurück. Verwenden Sie die setphysicalpresencerequest-Methode, um einen Vorgang anzufordern.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Getphysicalpresencerequest-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353861"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Getphysicalpresencerequest-Methode der Win32 \_ TPM-Klasse

Die **getphysicalpresencerequest** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse gibt den ausstehenden TPM-Anwesenheits Vorgang zurück. Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Ein-Wert, der den ausstehenden TPM-Anwesenheits Vorgang angibt.



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
<td><dl> <dt>1,0</dt> </dl></td>
<td>Keine Anforderung.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Aktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 2 rückgängig gemacht. <br/> Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Aktivieren</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>isEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht. <br/> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="disable-win32-tpm.md"><strong>Deaktivieren</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>€</dt> </dl></td>
<td>Aktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 4 rückgängig gemacht.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>0:</dt> </dl></td>
<td>Deaktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 3 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5@@</dt> </dl></td>
<td>Löschen Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/> Weitere Informationen finden Sie in der zugehörigen Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Aktivieren und aktivieren Sie das TPM. <br/> Dieser Vorgang wird von Vorgang 7 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>19.00</dt> </dl></td>
<td>Deaktivieren und deaktivieren Sie das TPM.<br/> Dieser Vorgang wird von Vorgang 6 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>88</dt> </dl></td>
<td>Ermöglicht die Installation eines TPM-Besitzers. <br/> Dieser Vorgang wird von Vorgang 9 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>21.00</dt> </dl></td>
<td>Verhindern Sie die Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 8 rückgängig gemacht. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>€</dt> </dl></td>
<td>Aktivieren, aktivieren und zulassen der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 11 rückgängig gemacht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11:</dt> </dl></td>
<td>Deaktivieren, deaktivieren und verhindern der Installation eines TPM-Besitzers.<br/> Dieser Vorgang wird von Vorgang 10 rückgängig gemacht.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>Verzögerte physische presenceunownedfieldupgrade<br/> Die Einstellung für die physische Anwesenheit wurde aktualisiert.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Löschen, aktivieren und aktivieren Sie das TPM.<br/> Dieser Vorgang kann nicht rückgängig gemacht werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17.15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird von Vorgang 16 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>Uhr</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Legt fest, dass die Bereitstellung nicht physisch vorhanden sein muss, um das TPM festzulegen.<br/> Dieser Vorgang wird von Vorgang 15 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>Uhr</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Hiermit wird die Bereitstellung festgelegt, die physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird durch den Vorgang 18 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>Jahren</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Hiermit wird die Bereitstellung festgelegt, die nicht physisch vorhanden sein muss, um das TPM zu löschen.<br/> Dieser Vorgang wird von Vorgang 17 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19.07.2016</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.<br/> Dieser Vorgang wird durch den Vorgang 20 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.<br/> Dieser Vorgang wird durch den Vorgang 19 rückgängig gemacht.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Aktivieren + aktivieren + löschen<br/> Aktivieren, aktivieren und Löschen des TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22.11.2016</dt> </dl></td>
<td>Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren<br/> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und aktivieren Sie dann das TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind die gemeinsamen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                      | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Die Methode war erfolgreich.<br/>                                                            |
| <dl> <dt>**TPM \_ E- \_ ppi- \_ ACPI- \_ Fehler**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ein Hardwarefehler ist aufgetreten. Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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

[**Klartext**](clear-win32-tpm.md)
</dt> <dt>

[**Deaktivieren**](disable-win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
