---
title: Informationen zur Bildmaster-API
description: Diese Dokumentation konzentriert sich auf eine Beschreibung der Adaptec-Implementierung von IMAPI für Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- Bildmastering-API IMAPI , beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb16ab8c542e7c4686c7a3f4d027169a520495a8d3fab9927f11ed974deeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451904"
---
# <a name="about-the-image-mastering-api"></a>Informationen zur Bildmaster-API

Diese Dokumentation konzentriert sich auf eine Beschreibung der Adaptec-Implementierung von IMAPI für Microsoft (IMAPIv1). Daher sind Beschreibungen der vier com-Hauptobjekte und deren Schnittstellen in diesem Dokument enthalten. Die vier Hauptobjekte lauten wie folgt: **MSDiscMasterObj,** **MSDiscRecorderObj,** **MSDiscStashObj** und **MS WiegeEngineObj**.

Auf einem System können **mehrere MSDiscMasterObj-Objekte** instanziiert werden, aber nur eine Anwendung kann gleichzeitig auf eine Aufzeichnung zugreifen. **MSDiscMasterObj implementiert** mehrere Schnittstellen, wie im folgenden Objektdiagramm dargestellt.

![msdiscmasterobj implementiert mehrere Schnittstellen](images/imapi.png)

Anwendungen verwenden die [**IDiscMaster-Schnittstelle,**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) um die folgenden Aufgaben auszuführen:

-   Öffnen von IMAPI
-   Aufzählen unterstützter Formate (Joliet und Redbook)
-   Auswählen eines Formats
-   Anzeigen einer Liste von Aufzeichnungen
-   Auswählen einer Aufzeichnung
-   Starten einer Brandung

Die [**Schnittstellen IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) und [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) werden über die [**IDiscMaster-Schnittstelle**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) an eine Anwendung zurückgegeben, wenn ein Format ausgewählt wird. Diese Schnittstellen steuern den Inhalt eines Daten- bzw. Audiodaten datenträgers. Es wird nicht erwartet, dass jede Anwendung die spezifischen Formatschnittstellen versteht. Anwendungen können auf generische Eigenschaften der **IJolietDiscMaster-Schnittstelle** zugreifen, z. B. Volumename oder Legacydateiname.

**Auf MSDiscRecorderObj-Objekte** wird über die [**IDiscRecorder-Schnittstelle**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) zugegriffen. Jedes CD-R- oder CD-RW-Gerät, das mit IMAPI kompatibel ist, verfügt über ein entsprechendes **MSDiscRecorderObj-Objekt.** Eine Anwendung verwendet Zeiger auf die **IDiscRecorder-Schnittstelle** für diese Objekte, um auszuwählen, welches Gerät von IMAPI zum Aufzeichnen einer CD verwendet wird. Darüber hinaus können Anwendungen über **IDiscRecorder** auf generische Eigenschaften eines Recorders zugreifen. Dies schließt Eigenschaften wie Schreibgeschwindigkeit oder andere Burn-Parameter ein.

Bei den verbleibenden **Objekten MSDiscStashObj** und **MSIghEngineObj** handelt es sich um interne Objekte, auf die von IMAPI zugegriffen wird. Sie werden hier nur erwähnt, um die IMAPI-Architektur zu verdeutlichen. **MSDiscStashObj** stellt (über die **IDiscStash-Schnittstelle)** eine Unformatierte Datei mit einer Größe von bis zu 800 MB dar, die von **MSDiscMasterObj** zum Erstellen von Audiobildern oder Zu verwendenden Datenträgern verwendet wird. Der Stash wird (über die **IMSEjEngine-Schnittstelle)** an **MS WiegineObj** übergeben, wenn eine Brandung von der Engine auf niedrigerer Ebene angefordert wird. Das **MSEjEngineObj-Objekt** erwartet, dass der Inhalt des Stashs in einem bekannten Format vor sich geht. In dieser Hinsicht verfügen **MSDiscMasterObj** und **MSEjEngineObj** über einen Vertrag in Bezug auf den Inhalt des Stashs.

 

 




