---
description: Stellt Funktionen für die Generierung von Zufallszahlen, Konvertierungen und Codierung und Decodierung von Base64 bereit.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Utilities-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368677"
---
# <a name="utilities-object"></a>Utilities-Objekt

\[Das Hilfsprogrammobjekt ist für die Verwendung in den Betriebssystemen verfügbar **, die im** Abschnitt "Anforderungen" angegeben sind.\]

Das **Utilities** -Objekt stellt Funktionen für die Zufallszahlengenerierung, Konvertierungen und Codierung und Decodierung von Base64 bereit.

## <a name="when-to-use"></a>Verwendung

Das **Utilities** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Codieren Sie eine Zeichenfolge als Base64, oder Decodieren Sie eine Zeichenfolge aus base64.
-   Konvertiert eine Binär gepackte Zeichenfolge in ein Bytearray und umgekehrt.
-   Konvertiert eine Binär gepackte Zeichenfolge in eine hexadezimale Zeichenfolge und umgekehrt.
-   Generieren Sie eine sichere Zufallszahl.
-   Konvertieren der Ortszeit in die koordinierte Weltzeit (Greenwich Mean Time) und umgekehrt.

## <a name="members"></a>Member

Das **Hilfsprogrammobjekt verfügt** über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **Utilities** -Objekt verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | Decodiert eine Zeichenfolge aus base64.<br/>                                     |
| [**Einem base64encode**](utilities-base64encode.md)                       | Codiert eine Zeichenfolge als Base64.<br/>                                       |
| [**Binarystringdebytearray**](utilities-binarystringtobytearray.md) | Konvertiert eine Binär Zeichen-Zeichenfolge in ein Bytearray.<br/>             |
| [**Binarydehex**](utilities-binarytohex.md)                         | Konvertiert eine Binär Zeichen-Zeichenfolge in eine hexadezimale Zeichenfolge.<br/>          |
| [**Bytearraydebinarystring**](utilities-bytearraytobinarystring.md) | Konvertiert ein Bytearray in eine Zeichenfolge mit Binär Zeichen.<br/>             |
| [**Getrandom**](utilities-getrandom.md)                             | Generiert eine sichere Zufallszahl.<br/>                                 |
| [**Hexin Binärdatei**](utilities-hextobinary.md)                         | Konvertiert eine hexadezimale Zeichenfolge in eine Zeichenfolge mit Binär Zeichen.<br/>          |
| [**Localtimetoutctime**](utilities-localtimetoutctime.md)           | Konvertiert die lokale Zeit des Computers in die koordinierte Weltzeit.<br/> |
| [**Utctimetolocaltime**](utilities-utctimetolocaltime.md)           | Konvertiert die koordinierte Weltzeit in die Ortszeit des Computers.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **Hilfsprogrammobjekt kann** erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Hilfsprogrammobjekt ist** CAPICOM. Hilfsprogramme. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




