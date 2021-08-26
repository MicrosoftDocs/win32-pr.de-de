---
title: Authentifizierungsebenen
description: Microsoft RPC bietet mehrere Authentifizierungsebenen.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cff12dae7331577da7748c2dc069bd6e7e4af6cfb1961f80d3de461930ddc3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080900"
---
# <a name="authentication-levels"></a>Authentifizierungsebenen

Microsoft RPC bietet mehrere Authentifizierungsebenen. Abhängig von der Authentifizierungsebene kann der Ursprung des Datenverkehrs (der vom Sicherheitsprinzipal gesendet wurde) überprüft werden, wenn die Verbindung hergestellt wird, wenn der Client einen neuen Remoteprozeduraufruf startet oder während jedes Paketaustauschs zwischen Client und Server.

Auch wenn der Absender des Datenverkehrs überprüft wird, ist die Sicherheit weiterhin schwach, da eine solche Überprüfung nicht sicherstellt, dass das Paket während der Weiterleitung nicht geändert oder beschädigt wurde. es wird nur überprüft, ob das Paket vom angegebenen Prinzipal stammt. Aus Sicherheitsgründen können verteilte Anwendungen die RPC-Laufzeitbibliothek festlegen, um zu überprüfen, ob keine der zwischen Client und Server ausgetauschten Daten geändert wird. Die RPC-Bibliothek kann auch den Inhalt jedes Pakets vor dem Senden verschlüsseln. Im Allgemeinen sollten Anwendungen, die ihren Datenverkehr schützen möchten, nur die letzten beiden Ebenen verwenden: Integrität und Datenschutz.

Beachten Sie, dass höhere Authentifizierungsebenen einen höheren Rechenaufwand erfordern. Als Entwickler müssen Sie entscheiden, welche Für Ihre Anwendung wichtiger ist – Geschwindigkeit oder Sicherheit. Die meisten Entwickler stellen fest, dass sie mit einigen Leistungstests akzeptable Leistungsstufen erreichen und gleichzeitig eine angemessene Sicherheit gewährleisten können.

Der Client und die Serverteile der verteilten Anwendung müssen die gleiche Authentifizierungsebene verwenden. Eine Liste der RPC-Authentifizierungsebenen finden Sie unter [Konstanten auf Authentifizierungsebene.](authentication-level-constants.md)

 

 




