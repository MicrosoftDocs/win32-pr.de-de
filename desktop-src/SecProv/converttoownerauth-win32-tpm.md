---
description: Übersetzt eine vom Benutzer bereitgestellte Passphraseeingabe in eine 20-Byte-Besitzerautorisierung, die für die Interaktion mit dem TPM verwendet werden kann. Methoden wie TakeOwnership und ResetAuthLockOut erfordern den resultierenden Besitzerautorisierungswert.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: ConvertToOwnerAuth-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 88d1b0f2056d6a10ac623421a7fe261acb832657d08c030ab3247f0acf1a0629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004648"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>ConvertToOwnerAuth-Methode der Win32 \_ Tpm-Klasse

Die **ConvertToOwnerAuth-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) übersetzt eine vom Benutzer bereitgestellte Passphraseeingabe in eine 20-Byte-Besitzerautorisierung, die für die Interaktion mit dem TPM verwendet werden kann. Methoden wie [**TakeOwnership**](takeownership-win32-tpm.md) und [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) erfordern den resultierenden Besitzerautorisierungswert.

Der Konvertierungsprozess folgt den Spezifikationen aus der [Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OwnerPassPhrase* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die in einen Besitzerautorisierungswert konvertiert werden soll. Die Zeichenfolge kann eine beliebige Anzahl alphanumerischer Zeichen enthalten.

</dd> <dt>

*OwnerAuth* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine vom *OwnerPassPhrase-Parameter abgeleitete* Zeichenfolge. Dieser Wert ist ein binärer 20-Byte-Wert, der in eine 28-Byte-Base64-Null-terminierte Zeichenfolge codiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

In den folgenden Tabellen sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine UTF-16LE-codierte Unicode-Zeichenfolge wird in den 20-Byte-TPM-Besitzerautorisierungswert konvertiert, indem der SHA-1-Hash der binären Darstellung der Zeichenfolge verwendet wird. Die **NULL-Terminierung** der Unicode-Zeichenfolge ist nicht im Hash enthalten. Im SHA-1-Hash wird kein Salt verwendet.

Um beispielsweise die TPM-Besitzerpassphrase "1Sample" in einen TPM-Besitzerautorisierungswert zu konvertieren, wird der SHA-1-Hash aus dem folgenden Bytestream entnommen:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Um eine Passphrase der Länge 0 (null) in einen Besitzerautorisierungswert zu konvertieren, wird der SHA-1-Hash aus dem NULL-Bytestream übernommen. 

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
