---
description: Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: SelfTest-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 42e0cf4e458be4ff95c05086d603f64d17fb7ff3c3da5a6781529d4632627f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891375"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a>SelfTest-Methode der Win32 \_ Tpm-Klasse

Die **SelfTest-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) führt einen Selbsttest des TPM durch und gibt das Ergebnis zurück.

Ein TPM-Selbsttest wird automatisch ausgeführt, wenn der Computer gestartet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SelfTestResult* \[ out\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das das Selbsttestergebnis enthält. Das Format dieses Parameters ist herstellerspezifisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

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
</dt> </dl>

 

 
