---
description: Aktiviert die automatische Bereitstellung des TPM, wenn es derzeit deaktiviert ist.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: Win32_Tpm::EnableAutoProvisioning-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 111073fc6f1a8c047182a33240c1cf1e7f3ed29260e9f7b1a390360dc6538c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891013"
---
# <a name="win32_tpmenableautoprovisioning-method"></a>Win32 \_ Tpm::EnableAutoProvisioning-Methode

Aktiviert die automatische Bereitstellung des TPM, wenn es derzeit deaktiviert ist. Der Vorgang hat keine Auswirkungen, wenn die automatische Bereitstellung bereits aktiviert ist. Standardmäßig ist die automatische Bereitstellung für Windows 8 und Windows Server 2012 aktiviert.

Auf diese Methode können nur lokale Administratoren zugreifen.

## <a name="syntax"></a>Syntax


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die spezifisch für [TPM-Basisdienste](../tbs/tbs-return-codes.md) sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
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

 

 
