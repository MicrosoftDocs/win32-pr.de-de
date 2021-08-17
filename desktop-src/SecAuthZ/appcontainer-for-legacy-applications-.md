---
description: Die AppContainer-Umgebung ist eine restriktive Prozessausführungsumgebung, die für Legacyanwendungen verwendet werden kann, um Ressourcensicherheit zu gewährleisten.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer für Legacyanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e0cdf21fc4008f1da0d55edb17abaf71978f4a5384843ecff60793b3d5b19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784733"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer für Legacyanwendungen

Die AppContainer-Umgebung ist eine restriktive Prozessausführungsumgebung, die für Legacyanwendungen verwendet werden kann, um Ressourcensicherheit zu gewährleisten. Eine Anwendung, die in einem AppContainer ausgeführt wird, kann nur auf Ressourcen zugreifen, die ihr speziell gewährt wurden. Daher können in einem AppContainer implementierte Anwendungen nicht gehackt werden, um böswillige Aktionen außerhalb der eingeschränkten zugewiesenen Ressourcen zu ermöglichen.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Vorteile der Verwendung einer AppContainer-Umgebung

Die AppContainer-Umgebung bietet sichere Sandboxing von Anwendungen. Dies isoliert die Anwendung vom Zugriff auf Hardware, Dateien, Registrierung, andere Anwendungen, Netzwerkkonnektivität und Netzwerkressourcen ohne bestimmte Berechtigung. Einzelne Ressourcen können als Ziel verwendet werden, ohne andere Ressourcen verfügbar zu machen. Darüber hinaus wird die Benutzeridentität mithilfe einer eindeutigen Identität geschützt, die eine Verkettung des Benutzers ist, und die App und Ressourcen werden mithilfe eines Modells mit den geringsten Rechten gewährt. Dies schützt darüber hinaus vor einer App, die die Identität des Benutzers antspricht, um Zugriff auf andere Ressourcen zu erhalten.

Weitere Informationen zur Verwendung von AppContainer für Legacyanwendungen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppContainer-Isolation](appcontainer-isolation.md)<br/>             | Isolation ist das Hauptziel einer AppContainer-Ausführungsumgebung. Durch die Isolierung einer Anwendung von nicht neded Resources und anderen Anwendungen werden Möglichkeiten für böswillige Manipulationen minimiert. Das Gewähren des Zugriffs auf der Grundlage der geringsten Rechte verhindert, dass Anwendungen und Benutzer über ihre Rechte hinaus auf Ressourcen zugreifen. Die Steuerung des Zugriffs auf Ressourcen schützt den Prozess, das Gerät und das Netzwerk.<br/> |
| [Implementieren eines AppContainers](implementing-an-appcontainer.md)<br/> | Ein AppContainer wird implementiert, indem dem Prozesstoken neue Informationen hinzugefügt und [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so geändert wird, dass alle älteren, unveränderten ACL-Objekte (Access Control List) standardmäßig Zugriffsanforderungen von AppContainer-Prozessen blockieren und ACL-Objekte erneut erstellen, die für AppContainers verfügbar sein sollten.<br/>                                                                                        |



 

 

