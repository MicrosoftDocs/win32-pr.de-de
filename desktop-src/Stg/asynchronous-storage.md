---
title: Asynchroner Speicher
description: Der asynchrone Speicher erweitert die strukturierte com-Speicher Spezifikation, um das asynchrone herunterladen von Speicher Objekten bei Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen.
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- Strukturierter Speicherplatz Halter-STG, asynchroner Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473796"
---
# <a name="asynchronous-storage"></a>Asynchroner Speicher

Der asynchrone Speicher erweitert die strukturierte com-Speicher Spezifikation, um das asynchrone herunterladen von Speicher Objekten bei Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen. Der asynchrone Speicher ermöglicht sowohl neuen als auch Legacy Anwendungen, die Verbund Dateien verwenden, ihren Inhalt effizient zu erzeugen, wenn über vorhandene Internet Protokolle darauf zugegriffen wird. Eine einzelne Anforderung an einen World Wide Web Server löst das Herunterladen von geschachtelten Objekten aus, die in einer Webseite enthalten sind. Dadurch entfällt die Notwendigkeit, jedes Objekt separat anzufordern. Ein asynchroner Download-und Zugriffs Mechanismus ermöglicht es einer Anwendung, die erste Seite der Daten zu erzeugen, bevor alle Daten empfangen wurden. Die genaue Reihenfolge, in der Elemente einer Seite verfügbar werden, kann vom webverleger angegeben werden und ist nicht von zufälligen Faktoren der Netzwerktopologie und Serververfügbarkeit abhängig.

Der asynchrone Speicher kann zusammen mit asynchronen Monikern verwendet werden, um ein umfassendes asynchrones Bindungsverhalten bereitzustellen. Weitere Informationen zu asynchronen Monikern finden Sie unter Microsoft ActiveX Software Development Kit. Ein Protokoll spezifischer asynchroner Moniker löst den Bindungs Vorgang aus und richtet die erforderlichen Komponenten ein. Im Internet Fall wäre dieser Moniker eine URL, die eine URL zum Binden an ein Objekt oder einen Speicher analysieren kann. Wenn das Ziel des Bindungs Vorgangs ein dauerhaftes Objekt ist, gibt der [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) -Rückruf ein asynchrones Speicher Objekt zurück.

> [!Note]  
> Die aktuelle Version der Microsoft-URL-Moniker unterstützt keinen asynchronen Speicher.

 

Ein asynchroner monikerclient fordert die asynchrone Bindung an, indem er ein BIND-Status-Rückruf Objekt implementiert und es beim Bindungs Kontext registriert. Das BIND-Status-Rückruf Objekt macht die [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstelle verfügbar, die es dem Client ermöglicht, Bindungs Einstellungen anzugeben und während eines Bindungs Vorgangs Status-und globale Daten Verfügbarkeits Benachrichtigungen zu empfangen. Die Implementierung der asynchronen Verbund Datei bietet einen Verbindungspunkt für [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), den Clients verwenden können, um bestimmte Verfügbarkeits Benachrichtigungen in einzelnen Streams zu empfangen.

 

 