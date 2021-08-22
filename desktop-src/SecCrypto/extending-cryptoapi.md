---
description: CryptoAPI wurde so konzipiert, dass es leicht erweiterbar ist. Neue Typen und Parameter können von jedem CSP-Autor (Cryptographic Service Provider) definiert werden, um CryptoAPI auf die Anforderungen einer Vielzahl von Situationen zu erfüllen.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Erweitern von CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0538e15f49e61dc26cacd4e81c42dd462aec092877428ebe865ab97c7729f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007019"
---
# <a name="extending-cryptoapi"></a>Erweitern von CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) wurde so konzipiert, dass es leicht erweiterbar ist. Neue Typen und Parameter können von jedem CSP-Autor [*(Cryptographic Service Provider)*](../secgloss/c-gly.md) definiert werden, damit CryptoAPI den Anforderungen einer Vielzahl von Situationen gerecht wird.



| Erweiterbare Elemente                                                                                                 | Kommentar                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anbietertypen<br/>                                                                                        | Ein Anbietertyp stellt eine bestimmte Familie oder einen Bestimmten Typ kryptografischer Dienste dar. Es können neue Anbietertypen definiert werden, die jeweils einen bestimmten Spezifischen bedienen.<br/>                                                                                                                                                                                                                                                                                          |
| Anbieterparameter<br/>                                                                                   | Anbieterparameter werden mit [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) bzw. [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**)gesendet und empfangen. Neue Anbieterparameter können es ermöglichen, einen CSP auf eine Weise zu konfigurieren, die nicht von den CryptoAPI-Designern beeinflusst wird.<br/>                                                                                                                                                                 |
| Algorithmusbezeichner<br/>                                                                                 | Die Enumerationsfunktionen von [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**) ermöglichen Anwendungen das dynamische Auflisten von Algorithmusbezeichnern. Neue [*symmetrische*](../secgloss/s-gly.md), [*öffentliche Schlüssel-*](../secgloss/p-gly.md)und [*Hashalgorithmen*](../secgloss/h-gly.md) können jederzeit definiert werden.<br/> |
| [*Öffentliche/private Schlüsselpaartypen*](../secgloss/p-gly.md)<br/> | Neue Schlüsselpaartypen können zwar nach Bedarf definiert werden, derzeit werden jedoch nur Signatur- und [*Schlüsselaustauschschlüsselpaare*](../secgloss/e-gly.md) verwendet.<br/>                                                                                                                                                                                                                                           |
| Schlüsselblobtypen<br/>                                                                                        | Neue [*Schlüssel-BLOB-Typen*](../secgloss/b-gly.md) können den flexiblen Austausch von Sitzungsschlüsseln, öffentlichen Schlüsseln und Paaren aus öffentlichen und privaten Schlüsseln mithilfe der Funktionen [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) und [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) ermöglichen.<br/>                                                                                                                                            |
| Schlüsselparameter<br/>                                                                                        | Schlüsselparameter werden mit [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) und [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**)gesendet und abgerufen. Neue Schlüsselparameter können die Unterstützung für viele verschiedene Arten von Schlüsseln ermöglichen.<br/>                                                                                                                                                                                                                         |
| Hashobjektparameter<br/>                                                                                | Hashobjektparameter werden mit [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) und [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**)gesendet und abgerufen. Neue Hashobjektparameter können die Unterstützung für viele verschiedene [*Hashtypen*](../secgloss/h-gly.md)ermöglichen.<br/>                                                                                                                                         |
| Flagwerte<br/>                                                                                           | Die meisten CryptoAPI-/CryptoSPI-Funktionen verfügen über einen *dwFlags-Parameter.* Neue *dwFlags-Werte* können das Verhalten von Funktionen nach Bedarf ändern.<br/>                                                                                                                                                                                                                                                                                                       |



 

Erweiterungen für CryptoAPI müssen auf verantwortungsvolle Weise vorgenommen werden. Bevor neue Parameter und Algorithmustypen definiert werden, sollte ein CSP-Entwickler Microsoft Corporation konsultieren, damit Folgendes zu beachten ist:

-   Allgemeine CryptoAPI-Erweiterungen können identifiziert und in der Wincrypt.h-Standarddatei platziert werden.
-   Namespacekonflikte können vermieden werden.
-   Es kann bestimmt werden, ob die Erweiterung erforderlich ist oder ob ein bestimmter Vorgang mithilfe der aktuellen API erreicht werden kann.

> [!Note]  
> Damit ein CSP mit Anwendungen kompatibel ist, die für den Microsoft Base Cryptographic Provider entwickelt wurden, muss er alle vorangehenden Elemente unterstützen, wie unter [Base Cryptography Functions](cryptography-functions.md) und [Cryptography Service Provider Functions](cryptography-functions.md)beschrieben.

 

 

 
