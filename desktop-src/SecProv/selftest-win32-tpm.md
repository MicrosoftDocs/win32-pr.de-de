---
description: Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Selftest-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348370"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a>Selftest-Methode der Win32- \_ TPM-Klasse

Die **Selftest** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse führt einen Selbsttest für das TPM aus und gibt das Ergebnis zurück.

Ein TPM-Self-Test wird automatisch ausgeführt, wenn der Computer gestartet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Selftestresult* \[ vorgenommen\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, das das Selbsttest Ergebnis enthält. Das Format dieses Parameters ist Hersteller spezifisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

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

 

 
