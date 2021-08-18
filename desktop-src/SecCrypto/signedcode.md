---
description: Stellt Funktionen zum Signieren ausführbarer Dateien mit einer digitalen Authenticode-Signatur zur Verfügung.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: SignedCode-Objekt
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
ms.openlocfilehash: e119a639af7cb6459e8e6ec8ae6416f9d067c56e8f81560fedc385abd518b840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899339"
---
# <a name="signedcode-object"></a>SignedCode-Objekt

\[Das **SignedCode-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) auf aufruft, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Das **SignedCode-Objekt** stellt Funktionen zum Signieren ausführbarer Dateien mit einer digitalen Authenticode-Signatur zur Verfügung.

## <a name="when-to-use"></a>Verwendung

Das **SignedCode-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Signieren ausführbarer Dateien.
-   Ausführbare Dateien mit Zeitstempel.
-   Bestimmen Sie, ob die Signatur der ausführbaren Datei gültig ist.
-   Legen Sie den Pfad zur ausführbaren Datei fest, oder rufen Sie diesen ab.
-   Rufen Sie den Signator und den Zeitstempel der ausführbaren Datei ab.
-   Rufen Sie eine Auflistung der Zertifikate für die ausführbare Datei ab.
-   Rufen Sie eine Beschreibung oder die URL zur Beschreibung der ausführbaren Datei ab.

## <a name="members"></a>Member

Das **SignedCode-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SignedCode-Objekt** verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zeichen**](signedcode-sign.md)           | Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**SignedCode.FileName-Eigenschaft angegeben**](signedcode-filename.md) ist.<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Erstellt eine Authenticode-Zeitstempelsignatur für die signierte ausführbare Datei, die in der [**SignedCode.FileName-Eigenschaft angegeben**](signedcode-filename.md) ist.<br/> |
| [**Überprüfung**](signedcode-verify.md)       | Überprüft die Authenticode-Signatur für die signierte ausführbare Datei, die in der [**SignedCode.FileName-Eigenschaft angegeben**](signedcode-filename.md) ist.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Das **SignedCode-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](signedcode-certificates.md)<br/>     | Schreibgeschützt<br/>  | Eine [**Zertifikatsammlung,**](certificates.md) die alle Zertifikate in der signierten ausführbaren Datei enthält.<br/>             |
| [**Beschreibung**](signedcode-description.md)<br/>       | Lesen/Schreiben<br/> | Eine Zeichenfolge, die eine Beschreibung der signierten ausführbaren Datei enthält.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lesen/Schreiben<br/> | Eine Zeichenfolge, die die HTTP-Adresse einer Beschreibung der signierten ausführbaren Datei enthält.<br/>                                         |
| [**Dateiname**](signedcode-filename.md)<br/>             | Lesen/Schreiben<br/> | Eine Zeichenfolge, die den Pfad zu der Inhaltsdatei enthält, die die ausführbare Datei enthält.<br/> Dies ist die Standardeigenschaft.<br/> |
| [**Signer**](signedcode-signer.md)<br/>                 | Schreibgeschützt<br/>  | Ein [**Signer-Objekt,**](signer.md) das Zugriff auf den Signator der ausführbaren Datei bietet.<br/>                                    |
| [**Zeitstempel**](signedcode-timestamper.md)<br/>       | Schreibgeschützt<br/>  | Ein [**Signer-Objekt,**](signer.md) das Zugriff auf den Zeitstempel der ausführbaren Datei bietet.<br/>                              |



 

## <a name="remarks"></a>Hinweise

Das **SignedCode-Objekt** kann erstellt werden und ist für die Skripterstellung nicht sicher. Die ProgID für das **SignedCode-Objekt** ist CAPICOM. SignedCode.1.

Die ausführbare Datei muss einen Typ haben, der mit Authenticode-Technologie signiert werden kann, z. B. Dateien mit der Dateierweiterung .cab, CAT, .exe, .dll, VBS oder OCX.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
