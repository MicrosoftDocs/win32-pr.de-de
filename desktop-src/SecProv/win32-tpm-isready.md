---
description: Gibt an, ob das TPM einsatzbereit ist.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: Win32_Tpm::IsReady-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8a04f2e834a77582698ff8f16e7a680db53474fa8c214556eb168c477afe58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004068"
---
# <a name="win32_tpmisready-method"></a>Win32 \_ Tpm::IsReady-Methode

Gibt an, ob das TPM einsatzbereit ist.

Auf diese Methode können nur lokale Administratoren zugreifen.

## <a name="syntax"></a>Syntax


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsReady* \[ out\]
</dt> <dd>

Legen Sie diese Einstellung auf **TRUE** fest, wenn TPM und System vollständig für die TPM-Verwendung bereitgestellt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die spezifisch für [TPM-Basisdienste](../tbs/tbs-return-codes.md) sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
