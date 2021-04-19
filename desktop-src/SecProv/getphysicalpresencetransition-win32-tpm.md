---
description: Gibt die Benutzeraktion an, die erforderlich ist, um den physischen Anwesenheits Vorgang Trusted Platform Module (TPM) auszuführen. Verwenden Sie die setphysicalpresencerequest-Methode, um einen Vorgang anzufordern.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Getphysicalpresencetransition-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352238"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Getphysicalpresencetransition-Methode der Win32- \_ TPM-Klasse

Die **getphysicalpresencetransition** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt die Benutzeraktion an, die zum Durchführen der physischen Anwesenheits Operation Trusted Platform Module (TPM) erforderlich ist. Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern. Die erforderliche Benutzeraktion ist für den Computer zum Zeitpunkt der Herstellung festgelegt. Normalerweise ist ein Neustart des Computers erforderlich.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Übergang* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Ein ganzzahliger Wert, der den Übergang angibt, der zum Ausführen eines physischen TPM-Anwesenheits Vorgangs erforderlich ist.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Es ist keine Benutzeraktion erforderlich, um einen physischen TPM-Anwesenheits Vorgang auszuführen.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Um einen physischen TPM-Anwesenheits Vorgang auszuführen, muss der Benutzer den Computer Herunterfahren und dann mithilfe des Schaltflächen Einschalten wieder einschalten. Der Benutzer muss physisch auf dem Computer anwesend sein, um die Änderung zu akzeptieren oder abzulehnen, wenn Sie vom BIOS aufgefordert werden.<br/> |
| <dl> <dt>2</dt> </dl> | Um einen physischen TPM-Anwesenheits Vorgang auszuführen, muss der Benutzer den Computer mithilfe eines warmen Neustarts neu starten. Der Benutzer muss physisch auf dem Computer anwesend sein, um die Änderung zu akzeptieren oder abzulehnen, wenn Sie vom BIOS aufgefordert werden.<br/>                              |
| <dl> <dt>3</dt> </dl> | Die erforderliche Benutzeraktion ist unbekannt.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



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

[**Setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
