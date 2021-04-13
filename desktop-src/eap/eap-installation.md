---
title: EAP-Installation
description: Anbieter implementieren eaps, auch als Authentifizierungsprotokolle bezeichnet, in Dynamic Link Libraries (DLLs).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389634"
---
# <a name="eap-installation"></a>EAP-Installation

Anbieter implementieren eaps, auch als Authentifizierungsprotokolle bezeichnet, in Dynamic Link Libraries (DLLs). Eine DLL für das Authentifizierungsprotokoll muss sowohl auf dem Client-als auch auf dem Server Computer gespeichert werden. Der Einfachheit halber können die Client-und Server-DLLs identisch sein. Dies ist jedoch keine Voraussetzung. Beachten Sie außerdem, dass dieselbe DLL mehr als ein Authentifizierungsprotokoll unterstützen kann.

Der Anbieter sollte Setup Software zum Installieren und Entfernen der DLL bereitstellen. Von der Setup Software sollten außerdem die entsprechenden Schlüssel und Werte für das Authentifizierungsprotokoll in der Systemregistrierung erstellt und bei der Deinstallation entfernt werden.

Die Installation der einzelnen EAP-dll sollte den folgenden Registrierungsschlüssel erstellen.

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

Im vorangehenden Pfad ist **&lt; eaptypeid &gt;** die ID des Authentifizierungs Protokolls. Der Anbieter muss diese ID von der Internet Assigned Numbers Authority (IANA) abrufen.

Weitere Informationen und eine Beschreibung der unterstützten Werte für diesen Schlüssel finden Sie unter [Registrierungs Werte für das Authentifizierungsprotokoll](authentication-protocol-registry-values.md).

 

 




