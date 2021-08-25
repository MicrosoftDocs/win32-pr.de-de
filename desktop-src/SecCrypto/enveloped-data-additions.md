---
description: Listet die Änderungen an den Funktionen zum Umgestalten von Daten auf.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Umschlag-Datenhinzufügungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75aab8e931ff8c8591a899a21a1071754e32f2e2cecec3755baa3dc64db94dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874420"
---
# <a name="enveloped-data-additions"></a>Umschlag-Datenhinzufügungen

Die folgenden Änderungen wurden an umschlageten Datenfunktionen vorgenommen:

-   Die Empfängeridentifikation kann nicht nur anhand des Ausstellers und der Seriennummer (PKCS \# 7 1.5), sondern auch anhand des Schlüsselbezeichners erfolgen.
-   Es werden drei Auswahlmöglichkeiten für den Austausch von Empfängerschlüsseln bereitgestellt:
    -   Schlüsseltransport mit RSA-Schlüsseln.
    -   Schlüsselvereinbarung mit Ephemeral-Static Diffie-Hellman Mit 3DES oder RC2 umschlossenen Algorithmusschlüsseln oder Ephemeral-Static Elliptic Curve Diffie-Hellman Mit AES umschlossenen Algorithmusschlüsseln.
    -   Schlüsselverschlüsselungsschlüssel oder Schlüsselübertragung der E-Mail-Liste, bei der der Zum Verschlüsseln des Inhaltsverschlüsselungsschlüssels verwendete Schlüssel bereits an die Empfänger verteilt wurde. RC2, 3DES und AES sind als Schlüsselumbruchalgorithmen zulässig.
-   Ungeschützte Attribute können in die Nachricht eingeschlossen werden.
-   Ein **OriginatorInfo-Feld** mit Informationen zum Absender wurde hinzugefügt, das Zertifikate und CRLs enthalten kann.
-   ECC-basierte Algorithmen (Elliptic Curve Cryptography) und AES erfordern Windows Vista oder höher.

 

 



