---
description: Die CryptoAPI-Nachrichten Funktionen entsprechen dem CMS- \# Standard (Cryptographic Message Syntax) von PKCS 7. Entwickler müssen mit dieser Spezifikation vertraut sein, um die Nachrichten Funktionen auf niedriger Ebene zu verwenden. Hier werden einige der Definitionen hervorgehoben.
ms.assetid: 99b633fe-9898-4570-ba8b-16ee78d351da
title: '\#Konzepte der kryptografischen Messaging Syntax von PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ead1c5e75737db80adbca725a30cb730b547be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360702"
---
# <a name="pkcs-7-cryptographic-messaging-syntax-concepts"></a>\#Konzepte der kryptografischen Messaging Syntax von PKCS 7

Die CryptoAPI-Nachrichten Funktionen entsprechen dem [CMS-Standard (Cryptographic Message Syntax)](https://www.ietf.org/rfc/rfc3369.txt)von [*PKCS \# 7*](../secgloss/p-gly.md) . Entwickler müssen mit dieser Spezifikation vertraut sein, um die [*Nachrichten Funktionen auf niedriger Ebene*](../secgloss/l-gly.md)zu verwenden. Hier werden einige der Definitionen hervorgehoben.

Der Standard "PKCS \# 7" beschreibt eine allgemeine Syntax für Daten, auf die [*Kryptografie*](../secgloss/c-gly.md) angewendet werden kann, z. b. [*digitale Signaturen*](../secgloss/d-gly.md) und [*digitale Umschläge*](../secgloss/d-gly.md). Die Syntax gibt eine Rekursion aus, sodass z. b. ein Umschlag innerhalb eines anderen Umschlags geschachtelt werden kann, oder eine Partei kann digitale Daten signieren, die bereits in einem Umschlag abgelegt wurden. Außerdem können beliebige Attribute, z. b. die Signatur Zeit, zusammen mit dem Inhalt einer Nachricht authentifiziert werden. Außerdem ermöglicht es anderen Attributen, z. b. [*countersignaturen*](../secgloss/c-gly.md), eine Signatur zugeordnet zu werden.

Der Datentyp, der in einer PKCS \# 7-Nachricht enthalten ist, wird als Inhaltstyp bezeichnet. Es gibt zwei Klassen von Inhaltstypen: Basis und erweitert.

-   Basis-Inhaltstypen enthalten nur Daten ohne kryptografische Erweiterungen. Aktuell gibt es nur einen Inhaltstyp in dieser Klasse, den [*Daten Inhaltstyp*](../secgloss/d-gly.md).
-   [*Erweiterte Inhaltstypen*](../secgloss/e-gly.md) enthalten Daten eines Typs (möglicherweise verschlüsselt) und anderer kryptografischer Erweiterungen (z. b. Hashes oder Signaturen).

Der Inhalt in der erweiterten Klasse verwendet Kapselung und gibt dabei die Begriffe [*äußerer Inhalt*](../secgloss/o-gly.md) (der, der die Erweiterungen enthält) und den [*inneren Inhalt*](../secgloss/i-gly.md) (der, der erweitert wird) an. Eine erweiterte Klasse kann z. b. den [*Daten Inhaltstyp*](../secgloss/d-gly.md) (Basisklasse) enthalten, in dem eine Signatur enthalten ist. In diesem Fall ist der Daten Inhaltstyp der *innere Inhalt* und die Kombination aus dem Daten Inhaltstyp und der Signatur bilden den äußeren Inhalt.

Die im PKCS 7-Standard definierten Inhaltstypen \# lauten wie folgt.



| Inhaltstyp              | Beschreibung                                                                                                                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Daten                      | Eine Zeichenfolge des Oktetts (**Byte**).                                                                                                                                                                                                                                                                                           |
| Signierte Daten               | Inhalt eines beliebigen Typs und verschlüsselter [*Nachrichtenhashes*](../secgloss/h-gly.md) ([*Digests*](../secgloss/m-gly.md)) des Inhalts für NULL oder mehr Signatur Geber.                                                                           |
| Eingeschlossene Daten            | Verschlüsselter Inhalt eines beliebigen Typs und verschlüsselter Inhalts Verschlüsselungsschlüssel für einen oder mehrere Empfänger. Die Kombination aus verschlüsseltem Inhalt und verschlüsseltem Inhalts Verschlüsselungsschlüssel für einen Empfänger ist ein [*digitaler Umschlag*](../secgloss/d-gly.md) für diesen Empfänger. |
| Signierte und eingehüllte Daten | Verschlüsselter Inhalt eines beliebigen Typs, verschlüsselter Content-Encryption-Schlüssel für einen oder mehrere Empfänger und doppelt verschlüsselte Nachrichten Digests für einen oder mehrere Unterzeichner. Die doppelte Verschlüsselung besteht aus einer Verschlüsselung mit dem privaten Schlüssel eines Signatur Gebers, gefolgt von einer Verschlüsselung mit dem Inhalts Verschlüsselungsschlüssel.                     |
| Verdauliche Daten             | Inhalt eines beliebigen Typs und ein Nachrichten [*Hash*](../secgloss/h-gly.md) (Digest) des Inhalts.                                                                                                                                                                                             |
| Verschlüsselte Daten            | Verschlüsselter Inhalt eines beliebigen Typs. Im Gegensatz zum [*Inhaltstyp*](../secgloss/d-gly.md)"Enveloped-Data" weist der verschlüsselte Daten Inhaltstyp weder Empfänger noch verschlüsselte Inhalts Verschlüsselungsschlüssel auf. Es wird davon ausgegangen, dass Schlüssel auf andere Weise verwaltet werden.               |



 

> [!Note]  
> In der Spezifikation der PKCS \# 7 beziehen sich die Begriffe [](../secgloss/d-gly.md) *Digest und Digest* auf den Wert, der durch Anwenden eines [*Hash Algorithmus*](../secgloss/h-gly.md) auf Daten erzeugt wird. In dieser Dokumentation werden die Begriffe [*Hash*](../secgloss/h-gly.md) und *thashed* für denselben Zweck verwendet. Beispielsweise wird der Datentyp, der mit den [*Nachrichten Funktionen auf niedriger Ebene*](../secgloss/l-gly.md) verwendet wird, als Hashwert bezeichnet und nicht als Fehler. Für den Zweck dieser Dokumentation können die beiden Sätze von Begriffen austauschbar verwendet werden.

 

 

 
