---
description: CryptoAPI ist so konzipiert, dass Sie problemlos erweiterbar ist. Neue Typen und Parameter können von jedem Autor eines Kryptografiedienstanbieters (kryptografischen Service Provider, CSP) definiert werden, damit CryptoAPI den Anforderungen einer Vielzahl von Situationen entspricht.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Erweitern der kryptoapi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62417f66b8a8bb2d06d145543f944f91868d366d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350129"
---
# <a name="extending-cryptoapi"></a>Erweitern der kryptoapi

[*CryptoAPI*](../secgloss/c-gly.md) ist so konzipiert, dass Sie problemlos erweiterbar ist. Neue Typen und Parameter können von jedem Autor eines [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) definiert werden, damit CryptoAPI den Anforderungen einer Vielzahl von Situationen entspricht.



| Erweiterbare Elemente                                                                                                 | Kommentar                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anbietertypen<br/>                                                                                        | Ein Anbietertyp stellt eine bestimmte Familie oder einen Typ von Kryptografiediensten dar. Es können neue Anbieter Typen definiert werden, von denen jeder eine bestimmte Nische bedient.<br/>                                                                                                                                                                                                                                                                                          |
| Anbieter Parameter<br/>                                                                                   | Anbieter Parameter werden mithilfe von [**cpsetprovparam**](https://www.bing.com/search?q=**CPSetProvParam**) bzw. [**cpgetprovparam**](https://www.bing.com/search?q=**CPGetProvParam**)gesendet und empfangen. Neue Anbieter Parameter können ermöglichen, dass ein CSP auf eine Weise konfiguriert wird, die von den CryptoAPI-Designern nicht geplant wurde.<br/>                                                                                                                                                                 |
| Algorithmusbezeichner<br/>                                                                                 | Die Enumerationsfunktionen von [**cpgetprovparam**](https://www.bing.com/search?q=**CPGetProvParam**) ermöglichen es Anwendungen, Algorithmusbezeichner dynamisch aufzulisten. Neue [*symmetrische*](../secgloss/s-gly.md), [*öffentliche Schlüssel*](../secgloss/p-gly.md)und [*Hash*](../secgloss/h-gly.md) Algorithmen können jederzeit definiert werden.<br/> |
| Paar Typen aus öffentlichem und [*privatem Schlüssel*](../secgloss/p-gly.md)<br/> | Während neue Schlüsselpaar Typen nach Bedarf definiert werden können, werden derzeit nur die Schlüssel [*Paare*](../secgloss/e-gly.md) für die Signatur und den Schlüsselaustausch verwendet.<br/>                                                                                                                                                                                                                                           |
| Schlüsselblob-Typen<br/>                                                                                        | Neue [*Schlüsselblob*](../secgloss/b-gly.md) -Typen können ermöglichen, dass Sitzungsschlüssel, öffentliche Schlüssel und öffentliche/private Schlüsselpaare auf flexible Weise mithilfe der Funktionen [**cpexportkey**](https://www.bing.com/search?q=**CPExportKey**) und [**cpimportkey**](https://www.bing.com/search?q=**CPImportKey**) ausgetauscht werden.<br/>                                                                                                                                            |
| Schlüsselparameter<br/>                                                                                        | Schlüsselparameter werden mithilfe von [**cpsetkeyparam**](https://www.bing.com/search?q=**CPSetKeyParam**) und [**cpgetkeyparam**](https://www.bing.com/search?q=**CPGetKeyParam**)gesendet und abgerufen. Neue Schlüsselparameter können die Unterstützung für viele verschiedene Schlüsseltypen ermöglichen.<br/>                                                                                                                                                                                                                         |
| Hash Objekt Parameter<br/>                                                                                | Hash Objekt Parameter werden mithilfe von [**cpsethashparam**](https://www.bing.com/search?q=**CPSetHashParam**) und [**cpgethashparam**](https://www.bing.com/search?q=**CPGetHashParam**)gesendet und abgerufen. Neue Hash Objekt Parameter können die Unterstützung für viele verschiedene Arten von [*Hashes*](../secgloss/h-gly.md)ermöglichen.<br/>                                                                                                                                         |
| Flagwerte<br/>                                                                                           | Die meisten CryptoAPI/cryptospi-Funktionen verfügen über einen *dwFlags* -Parameter. Neue *dwFlags* -Werte können das Verhalten von Funktionen nach Bedarf ändern.<br/>                                                                                                                                                                                                                                                                                                       |



 

Erweiterungen von CryptoAPI müssen auf verantwortungsbewusste Weise erstellt werden. Bevor Sie neue Parameter und Algorithmustypen definieren, sollte sich ein CSP-Entwickler an Microsoft Corporation wenden, um Folgendes zu tun:

-   Allgemeine CryptoAPI-Erweiterungen können identifiziert und in der standardmäßigen Wincrypt. h-Datei abgelegt werden.
-   Namespace Kollisionen können vermieden werden.
-   Mithilfe der aktuellen API kann ermittelt werden, ob die Erweiterung erforderlich ist oder ob ein bestimmter Vorgang erreicht werden kann.

> [!Note]  
> Damit ein CSP mit Anwendungen kompatibel ist, die für den Kryptografieanbieter von Microsoft entwickelt wurden, muss er alle vorangehenden Elemente unterstützen, wie unter [grundlegende Kryptografiefunktionen](cryptography-functions.md) und in [Kryptografiedienstanbieter-Funktionen](cryptography-functions.md)beschrieben.

 

 

 
