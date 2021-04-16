---
description: Erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Methode "kreateendorsegmentkeypair" der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525691"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Methode "kreateendorsegmentkeypair" der Win32- \_ TPM-Klasse

Die Methode " **kreateendorsegmentkeypair** " der [**Win32- \_ TPM**](win32-tpm.md) -Klasse erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM. Das Endorsement Key-Paar muss verfügbar sein, damit die [**TakeOwnership**](takeownership-win32-tpm.md) -Methode erfolgreich ausgeführt werden konnte. Sie können mit der [**isendorsementkeyplunpresent**](isendorsementkeypairpresent-win32-tpm.md) -Methode ermitteln, ob der Endorsement Key bereits auf dem TPM vorhanden ist.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                          |
| <dl> <dt> **TPM \_ E \_ deaktiviert \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Ein Endorsement Key-Paar ist bereits auf diesem TPM vorhanden.<br/> |



 

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
</dt> </dl>

 

 
