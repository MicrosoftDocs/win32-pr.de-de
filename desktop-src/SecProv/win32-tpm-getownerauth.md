---
description: Ruft die Besitzer Autorisierungs Informationen für ein TPM ab, sofern in der Registrierung eine verfügbar ist.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Win32_Tpm:: getownerauth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525667"
---
# <a name="win32_tpmgetownerauth-method"></a>Win32 \_ TPM:: getownerauth-Methode

Ruft die Besitzer Autorisierungs Informationen für ein TPM ab, sofern in der Registrierung eine verfügbar ist. Wenn ein TPM im Besitz von Windows 8 mit den Standardeinstellungen ist, werden die TPM-Besitzer Autorisierungs Informationen in der Registrierung gespeichert und können von dieser Methode verwendet werden.

Diese Methode ist nur für lokale Administratoren zugänglich.

## <a name="syntax"></a>Syntax


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Besitzer *des Besitzers* \[ vorgenommen\]
</dt> <dd>

Die Besitzer Autorisierungs Informationen für ein TPM, sofern in der Registrierung eine verfügbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
