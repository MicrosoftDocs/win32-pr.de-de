---
title: Informationen zur Image-Mastering-API
description: Diese Dokumentation konzentriert sich auf eine Beschreibung der Adaptec-Implementierung von IMAPI für Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- Image Mastering API IMAPI, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db1dc7846d2e47483abf2ca8856d593b874467f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104564548"
---
# <a name="about-the-image-mastering-api"></a>Informationen zur Image-Mastering-API

Diese Dokumentation konzentriert sich auf eine Beschreibung der Adaptec-Implementierung von IMAPI für Microsoft (IMAPIv1). Daher sind die Beschreibungen der vier Haupt-com-Objekte und deren Schnittstellen in diesem Dokument enthalten. Die vier Hauptobjekte lauten wie folgt: **msdiscmasterobj**, **msdiscrecorderobj**, **msdiscstashobj** und **msburnengineobj**.

Es können mehrere **msdiscmasterobj** -Objekte auf einem System instanziiert werden, aber nur eine Anwendung kann gleichzeitig auf einen Recorder zugreifen. **Msdiscmasterobj** implementiert mehrere Schnittstellen, wie im folgenden Objekt Diagramm gezeigt.

![msdiscmasterobj implementiert mehrere Schnittstellen](images/imapi.png)

Anwendungen verwenden die [**idiscmaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) -Benutzeroberfläche, um die folgenden Aufgaben auszuführen:

-   IMAPI öffnen
-   Unterstützte Formate auflisten (Joliet und Redbook)
-   Format auswählen
-   Eine Liste der Recorder erhalten
-   Aufzeichnung auswählen
-   Brennen starten

Wenn ein Format ausgewählt ist, werden die Schnittstellen [**ijolietdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) und [**iredbookdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) an eine Anwendung über die [**idiscmaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) -Schnittstelle zurückgegeben. Diese Schnittstellen steuern den Inhalt eines Datenträgers bzw. eines audiodatenträgers. Es wird nicht erwartet, dass jede Anwendung die spezifischen Format Schnittstellen versteht. Anwendungen können auf generische Eigenschaften der **ijolietdiscmaster** -Schnittstelle zugreifen, wie z. b. Volumename oder Legacy Dateiname.

Der Zugriff auf **msdiscrecorderobj** -Objekte erfolgt über die [**idiscrecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) -Schnittstelle. Jedes CD-R-oder CD-RW-Gerät, das mit IMAPI kompatibel ist, verfügt über ein entsprechendes **msdiscrecorderobj** -Objekt. Eine Anwendung verwendet Zeiger auf die **idiscrecorder** -Schnittstelle für diese Objekte, um auszuwählen, welches Gerät von IMAPI zum Aufzeichnen einer CD verwendet werden soll. Darüber hinaus können Anwendungen über **idiscrecorder** auf generische Eigenschaften einer Aufzeichnung zugreifen. Dies schließt Eigenschaften wie die Writer-Geschwindigkeit oder andere Verbrauchs Parameter ein.

Bei den verbleibenden Objekten, **msdiscstashobj** und **msburnengineobj**, handelt es sich um interne Objekte, auf die von IMAPI zugegriffen wird. Sie werden nur hier erwähnt, um die IMAPI-Architektur zu verdeutlichen. **Msdiscstashobj** stellt (über die **idiscstash** -Schnittstelle) eine Rohdatendatei mit einer Größe von bis zu 800 MB dar, die von **msdiscmasterobj** verwendet wird, um audiobilder oder zu bereinigende Datenscheiben zu erstellen. Der Stash wird an **msburnengineobj** (über die **imsburnengine** -Schnittstelle) übermittelt, wenn ein Burn-Wert von der untergeordneten Engine angefordert wird. Das **msburnengineobj** -Objekt erwartet, dass der Inhalt des Stash in einem bekannten Format vorliegt. In dieser Hinsicht haben **msdiscmasterobj** und **msburnengineobj** einen Vertrag bezüglich des Inhalts der Stash.

 

 




