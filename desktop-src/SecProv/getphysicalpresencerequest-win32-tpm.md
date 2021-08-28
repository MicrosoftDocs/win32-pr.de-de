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
ms.openlocfilehash: 7d88ec523e983e60cacab57b41307381b05e8de6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481866"
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




| Wert | Bedeutung | 
|-------|---------|
| <dl><dt>0</dt></dl> | Keine Anforderung.<br /> | 
| <dl><dt>1</dt></dl> | Aktivieren Sie das TPM.<br /> Dieser Vorgang wird durch Vorgang 2 rückgängig gemacht. <br /> Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten:<ul><li><a href="enable-win32-tpm.md"><strong>Aktivieren</strong></a></li><li><a href="isenabled-win32-tpm.md"><strong>isEnabled</strong></a></li></ul><br /> | 
| <dl><dt>2</dt></dl> | Deaktivieren Sie das TPM.<br /> Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht. <br /> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="disable-win32-tpm.md"><strong>Deaktivieren von</strong></a>.<br /> | 
| <dl><dt>3</dt></dl> | Aktivieren Sie das TPM.<br /> Dieser Vorgang wird durch Vorgang 4 rückgängig gemacht.<br /> | 
| <dl><dt>4</dt></dl> | Deaktivieren Sie das TPM.<br /> Dieser Vorgang wird durch Vorgang 3 rückgängig gemacht.<br /> | 
| <dl><dt>5</dt></dl> | Löschen Sie das TPM.<br /> Dieser Vorgang kann nicht rückgängig gemacht werden.<br /> Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Löschen Sie</strong></a>.<br /> | 
| <dl><dt>6</dt></dl> | Aktivieren und aktivieren Sie das TPM. <br /> Dieser Vorgang wird durch Vorgang 7 rückgängig gemacht.<br /> | 
| <dl><dt>7</dt></dl> | Deaktivieren und deaktivieren Sie das TPM.<br /> Dieser Vorgang wird durch Vorgang 6 rückgängig gemacht. <br /> | 
| <dl><dt>8</dt></dl> | Lassen Sie die Installation eines TPM-Besitzers zu. <br /> Dieser Vorgang wird durch Vorgang 9 rückgängig gemacht.<br /> | 
| <dl><dt>9</dt></dl> | Verhindert die Installation eines TPM-Besitzers.<br /> Dieser Vorgang wird durch Vorgang 8 rückgängig gemacht. <br /> | 
| <dl><dt>10</dt></dl> | Aktivieren, Aktivieren und Zulassen der Installation eines TPM-Besitzers.<br /> Dieser Vorgang wird durch Vorgang 11 rückgängig gemacht.<br /> | 
| <dl><dt>11</dt></dl> | Deaktivieren, deaktivieren und verhindern Sie die Installation eines TPM-Besitzers.<br /> Dieser Vorgang wird durch Vorgang 10 rückgängig gemacht.<br /> | 
| <span></span><dl><dt><strong></strong></dt><dt>12</dt></dl> | Deferred Physical PresenceunownedFieldUpgrade<br /> Die Einstellung für die physische Präsenz wurde aktualisiert.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>14</dt></dl> | Löschen, Aktivieren und Aktivieren des TPM.<br /> Dieser Vorgang kann nicht rückgängig gemacht werden.<br /> | 
| <dl><dt>15</dt></dl> | SetNoPPIProvision_False<br /> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM festlegen zu können.<br /> Dieser Vorgang wird durch Vorgang 16 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>16</dt></dl> | SetNoPPIProvision_True<br /> Legt die Bereitstellung fest, die sie nicht physisch benötigen, um das TPM festlegen zu können.<br /> Dieser Vorgang wird durch Vorgang 15 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>17</dt></dl> | SetNoPPIClear_False<br /> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu löschen.<br /> Dieser Vorgang wird durch Vorgang 18 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>18</dt></dl> | SetNoPPIClear_True<br /> Legt die Bereitstellung fest, die sie nicht physisch benötigen, um das TPM zu löschen.<br /> Dieser Vorgang wird durch Vorgang 17 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIMaintenance_False<br /> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu verwalten.<br /> Dieser Vorgang wird durch Vorgang 20 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>20</dt></dl> | SetNoPPIMaintenance_True<br /> Legt die Bereitstellung fest, dass Sie physisch sein müssen, um das TPM zu verwalten.<br /> Dieser Vorgang wird durch Vorgang 19 rückgängig gemacht.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>21</dt></dl> | Aktivieren + Aktivieren + Löschen<br /> Aktivieren, aktivieren und löschen Sie das TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 
| <dl><dt>22</dt></dl> | Aktivieren + Aktivieren + Löschen + Aktivieren + Aktivieren<br /> Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und reaktivieren Sie das TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.<br /> | 




 

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

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

[**Clear**](clear-win32-tpm.md)
</dt> <dt>

[**Deaktivieren**](disable-win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> <dt>

[**isEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
