---
description: Die HTTP-Authentifizierung mit Microsoft Digest erfordert drei Eingabepuffer, um eine Abfrage Antwort zu generieren. In der folgenden Tabelle werden diese Puffer zusammengefasst.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Eingabepuffer für die digestaufforderungs-Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128305"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Eingabepuffer für die digestaufforderungs-Antwort

Die HTTP-Authentifizierung mit Microsoft Digest erfordert drei Eingabepuffer, um eine Abfrage Antwort zu generieren. In der folgenden Tabelle werden diese Puffer zusammengefasst.



| Puffer Nummer | Enthält                                                                                                                                             | Puffertyp                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Vom Server empfangene Abfrage                                                                                                                   | secbuffer- \_ Token                                            |
| 1             | HTTP-Methode                                                                                                                                          | secbuffer \_ -Parameter                                           |
| 2             | H (Entität)                                                                                                                                            | secbuffer \_ -Parameter                                           |
| 3             | Der [*Dienst Prinzipal Name (Service Principal Name*](../secgloss/s-gly.md) , SPN) des Zielservers. | **Secbuffer \_ Schreib \_** Schutz für \| **secbuffer \_** des Zielhosts      |
| 4             | Werte für Kanal Bindungs Token                                                                                                                        | **Secbuffer \_ Kanal \_ Bindungen** \| **secbuffer \_** schreibgeschützt |



 

Der Puffer NULL enthält die vom Server empfangene digestfrage als Antwort auf die anfängliche Anforderung einer Zugriffs geschützten Ressource.

Buffer 1 enthält die Zeichen folgen Darstellung der Methode, z. b. "Get" oder "Post". Die-Methode wird in der Berechnung von a2 verwendet, wie in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)beschrieben.

Buffer 2 ist der [*MD5*](../secgloss/m-gly.md) -Hash des Entitäts Texts der Nachricht, wie in RFC 2617 beschrieben.

Buffer 3 enthält den SPN des Zielservers in UTF-8-Formatierung, wenn Digest mit Kanal Bindungen verwendet wird.

Puffer 4 enthält den channelbindungstokenwert, wenn Digest mit Kanal Bindungen verwendet wird.

## <a name="input-buffers-for-sasl"></a>Eingabepuffer für SASL

Stellen Sie nur Puffer NULL bereit. Aus Gründen der Kompatibilität mit anderen SSPs können Sie [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) ohne gültige Server Herausforderung abrufen. In diesem Fall sollte der *pinput* -Parameter auf **null** festgelegt werden.

 

 
