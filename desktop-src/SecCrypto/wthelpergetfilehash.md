---
description: Überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Wthelpergetflehash-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959863"
---
# <a name="wthelpergetfilehash-function"></a>Wthelpergetflehash-Funktion

\[Die **wthelpergetflehash** -Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **wthelpergetflehash** -Funktion überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.

> [!Note]  
> Diese Funktion ist nicht in einer veröffentlichten Header Datei deklariert. Um diese Funktion zu verwenden, deklarieren Sie Sie im exakten Format. Diese Funktion hat auch keine zugehörige Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Wintrust.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszFileName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad und den Dateinamen der Datei enthält, für die der Hash erhalten werden soll.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte NULL sein.

</dd> <dt>

*pvReserved* \[ in, out, optional\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte **null** sein.

</dd> <dt>

*pbflehash* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, um den Hashwert für die Datei zu erhalten. Der *pcbflehash* -Parameter enthält die Größe dieses Puffers.

</dd> <dt>

*pcbflehash* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine **DWORD** -Variable, die bei der Eingabe die Größe des *pbflehash* -Puffers in Bytes enthält und bei der Ausgabe die Größe des Hashwerts in Bytes empfängt.

Um die erforderliche Größe des Hashwerts zu erhalten, übergeben Sie **null** für den *pbflehash* -Parameter. Diese Funktion platziert die erforderliche Größe (in Bytes) des Hashwerts an diesem Speicherort.

Wenn der *pbsplehash* -Parameter nicht **null** ist und die Größe nicht groß genug ist, um den Hashwert zu erhalten, platziert diese Funktion die erforderliche Größe in Byte an diesem Speicherort und gibt **Fehler \_ Weitere \_ Daten** zurück.

</dd> <dt>

*phashalgid* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**ALG- \_ ID**](alg-id.md) -Variable, die den Bezeichner des Algorithmus empfängt, der zum Erstellen des Hashwerts verwendet wird. Dieser Parameter kann **null** sein, wenn diese Informationen nicht benötigt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Statuscode zurück, der angibt, ob die Funktion erfolgreich war oder fehlgeschlagen ist.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler \_ erfolgreich**</dt> </dl>             | Die Datei ist signiert, und die Signatur wurde überprüft.<br/>                                                                                        |
| <dl> <dt>**Fehler \_ Weitere \_ Daten**</dt> </dl>          | Der *pbsplehash* -Parameter ist nicht **null**, und die vom *pcbflehash* -Parameter angegebene Größe ist nicht groß genug, um den Hash zu empfangen.<br/> |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl> | Es ist ein Fehler bei der Speicher Belegung aufgetreten.<br/>                                                                                                      |
| <dl> <dt>**fehlerhafter \_ \_ \_ Digest**</dt> </dl>      | Die Signatur der Datei wurde nicht überprüft.<br/>                                                                                                |
| <dl> <dt>**\_e \_ NoSignature Vertrauen**</dt> </dl>      | Die Datei wurde nicht signiert oder enthielt eine ungültige Signatur.<br/>                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
