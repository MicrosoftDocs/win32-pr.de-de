---
description: Die IsEnabled-Methode der Win32 \_ Tpm-Klasse gibt an, ob das Gerät aktiviert ist. Dieser Wert kann mit den Methoden Enable und Disable geändert werden.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: IsEnabled-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1d61c96d9c80ae77f9869261905fb93461530b452deaf7a4709b394623a3dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667500"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>IsEnabled-Methode der Win32 \_ Tpm-Klasse

Die **IsEnabled-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt an, ob das Gerät aktiviert ist. Dieser Wert kann mit den Methoden [**Enable und**](enable-win32-tpm.md) [**Disable geändert**](disable-win32-tpm.md) werden.

## <a name="syntax"></a>Syntax


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsEnabled* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

True **gibt an,** dass das Gerät aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Gemäß der spezifikation Trusted Computing Group (TCG) v1.2 sind nur die folgenden Befehle verfügbar, wenn sich das Gerät in einem deaktivierten Zustand befindet.

-   TPM \_ ContinueSelfTest
-   TPM \_ DSAP
-   TPM \_ FlushSpecific
-   TPM \_ GetCapability
-   TPM \_ GetTestResult
-   \_TPM-Init
-   \_TPM-OIAP
-   TPM \_ OSAP
-   TPM \_ OwnerSetDisable
-   \_TPM-PCR-Zurücksetzung \_
-   TPM \_ PhysicalDisable
-   TPM \_ PhysicalEnable
-   TPM \_ PhysicalSetDeactivated
-   \_TPM-Zurücksetzung
-   TPM \_ SaveState
-   TPM \_ SelfTestFull
-   TPM \_ SetCapability
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   \_TPM-Start
-   TPM \_ TakeOwnership
-   TPM \_ Terminate \_ Handle

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

[**Deaktivieren**](disable-win32-tpm.md)
</dt> <dt>

[**Aktivieren**](enable-win32-tpm.md)
</dt> </dl>

 

 
