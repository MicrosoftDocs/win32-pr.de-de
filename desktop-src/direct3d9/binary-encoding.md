---
description: In diesem Abschnitt wird die binäre Version des DirectX-Dateiformats (.x) beschrieben, die mit der Veröffentlichung von DirectX 3.0 eingeführt wurde.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Binärcodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f35d4ccd33692cc25c2b99c8c20ed53dc0c7a01a488c738992a9a4f22fbc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460759"
---
# <a name="binary-encoding"></a>Binärcodierung

In diesem Abschnitt wird die binäre Version des DirectX-Dateiformats (.x) beschrieben, die mit der Veröffentlichung von DirectX 3.0 eingeführt wurde.

Das Binärformat ist eine tokenisierte Darstellung des Textformats. Token können eigenständig sein oder von primitiven Datensätzen begleitet werden. Eigenständige Token bieten eine grammatikalische Struktur, und Datensatztoken stellen die erforderlichen Daten zur Verfügung.

Beachten Sie, dass alle Daten im Little-Endian-Format gespeichert werden. Ein gültiger binärer Datenstrom besteht aus einem Header gefolgt von Vorlagen und/oder Datenobjekten.

In diesem Abschnitt werden die folgenden Komponenten des Binärdateiformats erläutert und eine Beispielvorlage und ein Binärdatenobjekt zur Verfügung gestellt.

-   [Header](header.md)
-   [Token](tokens.md)
-   [Tokendatensätze](token-records.md)
-   [Vorlagen](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [Daten](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [Beispiele](examples.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateiformatreferenz](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



