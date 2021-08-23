---
description: Importiert die Autorisierungsinformationen des Besitzers für ein TPM, das sich bereits im Besitz der Betriebssystemregistrierung befindet.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: Win32_Tpm::ImportOwnerAuth-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6e7d96a5cadf77e539d703ed95f428fa91535d49d1e7b5581300467782fce0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004078"
---
# <a name="win32_tpmimportownerauth-method"></a>Win32 \_ Tpm::ImportOwnerAuth-Methode

Importiert die Autorisierungsinformationen des Besitzers für ein TPM, das sich bereits im Besitz der Betriebssystemregistrierung befindet. Bei diesem Vorgang wird zunächst überprüft, ob die angegebenen Autorisierungsinformationen des Besitzers korrekt sind. Wenn dies der Fall ist, importiert die -Methode diese Informationen in die Registrierung.

Auf diese Methode kann nur von lokalen Administratoren zugegriffen werden.

## <a name="syntax"></a>Syntax


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OwnerAuth* \[ In\]
</dt> <dd>

Die gültigen Besitzerautorisierungsinformationen für das TPM.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler und -Fehler, die für [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ist besonders nützlich in Szenarien, in denen sich das TPM in einem "Bereit mit eingeschränktem Funktionszustand" befindet und erfordert, dass der Import der Besitzerautorisierung vollständig bereit ist, oder in Dual-Boot-Szenarien, in denen eines der Betriebssysteme das TPM besitzt und die Besitzerautorisierungsinformationen für TPM im anderen Betriebssystem nicht verfügbar sind.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ \\ CIMV2-Sicherheit \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
