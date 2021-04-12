---
title: Authentifizierungs Ebenen
description: Microsoft RPC bietet mehrere Authentifizierungs Ebenen.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206710"
---
# <a name="authentication-levels"></a>Authentifizierungs Ebenen

Microsoft RPC bietet mehrere Authentifizierungs Ebenen. Abhängig von der Authentifizierungs Ebene kann der Ursprung des Datenverkehrs (welcher Sicherheits Prinzipal den Datenverkehr gesendet hat) überprüft werden, wenn die Verbindung hergestellt wird, wenn der Client einen neuen Remote Prozedur aufzurufen startet oder während jedes Paket Austauschs zwischen Client und Server.

Auch wenn der Absender des Datenverkehrs überprüft wird, ist die Sicherheit weiterhin schwach, da bei dieser Überprüfung nicht sichergestellt wird, dass das Paket nicht geändert oder beschädigt wurde. Es wird nur überprüft, ob das Paket vom angegebenen Prinzipal stammt. Um die Sicherheit zu erhöhen, können verteilte Anwendungen die RPC-Lauf Zeit Bibliothek festlegen, um sicherzustellen, dass keine der zwischen Client und Server ausgetauschten Daten geändert wird. Die RPC-Bibliothek kann auch den Inhalt jedes Pakets verschlüsseln, bevor Sie gesendet wird. Im Allgemeinen sollten Anwendungen, die Ihren Datenverkehr sichern möchten, nur die letzten zwei Ebenen verwenden – Integrität und Datenschutz.

Beachten Sie, dass ein höheres Maß an Authentifizierung einen höheren Berechnungs Aufwand erfordert. Als Entwickler müssen Sie sich entscheiden, was für Ihre Anwendung wichtiger ist – Geschwindigkeit oder Sicherheit. Die meisten Entwickler werden feststellen, dass Sie bei einigen Leistungstests akzeptable Leistungsstufen erzielen und gleichzeitig eine angemessene Sicherheit gewährleisten können.

Die Client-und Server Teile der verteilten Anwendung müssen die gleiche Authentifizierungs Ebene verwenden. Eine Liste der RPC-Authentifizierungs Ebenen finden Sie unter [Konstanten auf Authentifizierungs Ebene](authentication-level-constants.md).

 

 




