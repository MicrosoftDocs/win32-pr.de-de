---
description: Ruft den Storage Stammschlüsselfingerabdruck für einen angegebenen Modulus des öffentlichen Teils des TPM-Storage Stammschlüssels ab.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: Win32_Tpm::GetSrkADThumbprint-Methode
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
ms.openlocfilehash: 9be4b7f02a9b645c29b431a9d974f5871ad5a95fc001e43df17bfe459483974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004108"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ Tpm::GetSrkADThumbprint-Methode

Ruft den Storage Stammschlüsselfingerabdruck für einen angegebenen Modulus des öffentlichen Teils des TPM-Storage Stammschlüssels ab. Der Fingerabdruck wird zum Indizierung der Storage Stammschlüssel auf dem Active Directory-Server verwendet, wenn die Active Directory-Sicherung der TPM-Besitzerautorisierungsinformationen über Gruppenrichtlinie Einstellung aktiviert ist.

> [!Note]  
> Ab Windows 10 Version 1607 wird die TPM-Besitzerautorisierung nie in Active Directory gesichert.

 

Auf diese Methode können nur lokale Administratoren zugreifen.

## <a name="syntax"></a>Syntax


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SrkPublicKeyModulus* \[ In\]
</dt> <dd>

Der Modulus des öffentlichen Teils des TPM-Storage Stammschlüssels. Sie kann auch mit der [**GetSrkPublicKeyModulus-Methode**](win32-tpm-getsrkpublickeymodulus.md) der [Win32 \_ TPM-Klasse](win32-tpm.md) abgerufen werden.

</dd> <dt>

*SrkADThumbprint* \[ out\]
</dt> <dd>

Gibt ein 20-Byte-Array zurück, das den Stammschlüsselfingerabdruck des Speichers für den angegebenen Modulus enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die spezifisch für [TPM-Basisdienste](../tbs/tbs-return-codes.md) sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
