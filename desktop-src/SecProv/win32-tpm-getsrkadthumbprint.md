---
description: Ruft den Speicher Stamm Schlüssel-Fingerabdruck für einen angegebenen Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels ab.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm:: gezrkadthumbprint-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344423"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ TPM:: gezrkadthumbprint-Methode

Ruft den Speicher Stamm Schlüssel-Fingerabdruck für einen angegebenen Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels ab. Der Fingerabdruck wird zum Indizieren der Speicher Stamm Schlüssel auf dem Active Directory Server verwendet, wenn die Active Directory Sicherung der TPM-Besitzer Autorisierungs Informationen durch Gruppenrichtlinie Einstellung aktiviert ist.

> [!Note]  
> Ab Windows 10, Version 1607, wird die TPM-Besitzer Autorisierung nie auf Active Directory gesichert.

 

Diese Methode ist nur für lokale Administratoren zugänglich.

## <a name="syntax"></a>Syntax


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Srkpublickeymodulus* \[ in\]
</dt> <dd>

Der Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels. Sie kann auch mithilfe der [**getrkpublickeymodulus**](win32-tpm-getsrkpublickeymodulus.md) -Methode der [Win32 \_ TPM](win32-tpm.md) -Klasse abgerufen werden.

</dd> <dt>

*Srkadthumbprint* \[ vorgenommen\]
</dt> <dd>

Gibt ein 20-Byte-Array zurück, das den Speicher Stamm Schlüssel-Fingerabdruck für den angegebenen Modulus enthält.

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

 

 
