---
description: Stellt Funktionen zum Signieren von ausführbaren Dateien mit einer digitalen Authenticode-Signatur bereit.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Signedcode-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365658"
---
# <a name="signedcode-object"></a>Signedcode-Objekt

\[Das **signedcode** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Das **signedcode** -Objekt stellt Funktionen zum Signieren von ausführbaren Dateien mit einer digitalen Authenticode-Signatur bereit.

## <a name="when-to-use"></a>Verwendung

Das **signedcode** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Signieren Sie ausführbare Dateien.
-   Ausführbare Dateien für Zeitstempel.
-   Bestimmen Sie, ob die Signatur der ausführbaren Datei gültig ist.
-   Legen Sie den Pfad zur ausführbaren Datei fest oder rufen Sie ihn ab.
-   Rufen Sie den Signatur Geber und den Zeitstempel der ausführbaren Datei ab.
-   Ruft eine Sammlung der Zertifikate für die ausführbare Datei ab.
-   Rufen Sie eine Beschreibung oder die URL zur Beschreibung der ausführbaren Datei ab.

## <a name="members"></a>Member

Das **signedcode** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **signedcode** -Objekt verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gebärden**](signedcode-sign.md)           | Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.<br/> |
| [**Weisen**](signedcode-verify.md)       | Überprüft die Authenticode-Signatur in der signierten ausführbaren Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Das **signedcode** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](signedcode-certificates.md)<br/>     | Schreibgeschützt<br/>  | Eine [**Zertifikat**](certificates.md) Sammlung, die alle Zertifikate in der signierten ausführbaren Datei enthält.<br/>             |
| [**Beschreibung**](signedcode-description.md)<br/>       | Lesen/Schreiben<br/> | Eine Zeichenfolge, die eine Beschreibung der signierten ausführbaren Datei enthält.<br/>                                                             |
| [**Deskriptionurl**](signedcode-descriptionurl.md)<br/> | Lesen/Schreiben<br/> | Eine Zeichenfolge, die die http-Adresse für eine Beschreibung der signierten ausführbaren Datei enthält.<br/>                                         |
| [**FileName**](signedcode-filename.md)<br/>             | Lesen/Schreiben<br/> | Eine Zeichenfolge, die den Pfad zur Inhalts Datei enthält, die die ausführbare Datei enthält.<br/> Dies ist die Standard Eigenschaft.<br/> |
| [**Signatur Geber**](signedcode-signer.md)<br/>                 | Schreibgeschützt<br/>  | Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Signatur Geber der ausführbaren Datei bereitstellt.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Schreibgeschützt<br/>  | Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Zeitstempel der ausführbaren Datei bereitstellt.<br/>                              |



 

## <a name="remarks"></a>Bemerkungen

Das **signedcode** -Objekt kann erstellt werden und ist für die Skripterstellung nicht sicher. Die ProgID für das **signedcode** -Objekt ist CAPICOM. Signedcode. 1.

Die ausführbare Datei muss einen Typ aufweisen, der mit Authenticode-Technologie signiert werden kann, z. b. Dateien mit der Dateinamenerweiterung ". cab", ". cat", ". exe", ". dll", ". vb" oder ". ocx".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
