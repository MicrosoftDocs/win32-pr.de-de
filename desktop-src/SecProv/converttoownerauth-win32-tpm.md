---
description: Übersetzt eine vom Benutzer bereitgestellte Passphrase-Eingabe in eine 20-Byte-Besitzer Autorisierung, die für die Interaktion mit dem TPM verwendet werden kann. Methoden wie TakeOwnership und resetauthlockout erfordern den resultierenden Besitzer Autorisierungs Wert.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Converttbesitzauth-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358589"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Converttbesitzauth-Methode der Win32- \_ TPM-Klasse

Die **converttobesitzauth** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse übersetzt eine vom Benutzer bereitgestellte Passphrase-Eingabe in eine 20-Byte-Besitzer Autorisierung, die für die Interaktion mit dem TPM verwendet werden kann. Methoden wie [**TakeOwnership**](takeownership-win32-tpm.md) und [**resetauthlockout**](resetauthlockout-win32-tpm.md) erfordern den resultierenden Besitzer Autorisierungs Wert.

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

Besitzer *Passphrase* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die in einen Besitzer Autorisierungs Wert konvertiert werden soll. Die Zeichenfolge kann eine beliebige Anzahl von alphanumerischen Zeichen enthalten.

</dd> <dt>

Besitzer *des Besitzers* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die vom Besitzer *Passphrase* -Parameter abgeleitet ist. Dieser Wert ist ein 20-Byte-Binärwert, der in eine mit **null** endender Base64-NULL endenden Zeichenfolge codiert ist

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Unicode-UTF-16LE-codierte Zeichenfolge wird in den 20-Byte-TPM-Besitzer Autorisierungs Wert konvertiert, indem der SHA-1-Hash der binären Darstellung der Zeichenfolge verwendet wird. Der **null** -Abbruch der Unicode-Zeichenfolge ist nicht im Hash enthalten. Im SHA-1-Hash wird kein Salt verwendet.

Wenn Sie z. b. die TPM-Besitzer Passphrase "1sample" in einen TPM-Besitzer Autorisierungs Wert konvertieren möchten, wird der SHA-1-Hash aus dem folgenden Bytestream entnommen:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Um eine Passphrase der Länge 0 (null) in einen Besitzer Autorisierungs Wert zu konvertieren, wird der SHA-1-Hash aus dem **null** -Bytestream entnommen.

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
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
