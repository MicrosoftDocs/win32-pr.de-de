---
description: Gibt die Benutzeraktion an, die erforderlich ist, um den physischen Trusted Platform Module (TPM) durchzuführen. Verwenden Sie die SetPhysicalPresenceRequest-Methode, um einen Vorgang anfordern.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: GetPhysicalPresenceTransition-Methode der Win32_Tpm Klasse
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
ms.openlocfilehash: 939f29d923182d3e2b0b9237c49c2a5fc6ff8652d2361f867a7e95af48415654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906340"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>GetPhysicalPresenceTransition-Methode der Win32 \_ Tpm-Klasse

Die **GetPhysicalPresenceTransition-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt die Benutzeraktion an, die erforderlich ist, um den physischen Anwesenheitsvorgang Trusted Platform Module (TPM) durchzuführen. Verwenden Sie [**die SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um einen Vorgang anfordern. Die erforderliche Benutzeraktion wird für Ihren Computer zum Zeitpunkt der Herstellung festgelegt. In der Regel ist ein Neustart des Computers erforderlich.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Übergang* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein ganzzahliger Wert, der den Übergang angibt, der zum Ausführen eines TPM-Vorgangs für die physische Präsenz erforderlich ist.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Es ist keine Benutzeraktion erforderlich, um einen TPM-Vorgang für die physische Präsenz durchzuführen.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Um einen PHYSISCHEN TPM-Anwesenheitsvorgang durchzuführen, muss der Benutzer den Computer herunterfahren und dann mithilfe des Netzschalters wieder einschalten. Der Benutzer muss physisch auf dem Computer vorhanden sein, um die Änderung zu akzeptieren oder abzulehnen, wenn er vom BIOS dazu aufgefordert wird.<br/> |
| <dl> <dt>2</dt> </dl> | Um einen PHYSISCHEN TPM-Anwesenheitsvorgang durchzuführen, muss der Benutzer den Computer mithilfe eines warmen Neustarts neu starten. Der Benutzer muss physisch auf dem Computer vorhanden sein, um die Änderung zu akzeptieren oder abzulehnen, wenn er vom BIOS dazu aufgefordert wird.<br/>                              |
| <dl> <dt>3</dt> </dl> | Die erforderliche Benutzeraktion ist unbekannt.<br/>                                                                                                                                                                                                                |



 

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

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
