---
description: Anwendungsspezifische Leistungsindikatoren können Ihnen helfen, die Leistung beim Entwickeln und Debuggen der Anwendung zu optimieren.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Hinzufügen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaf66d6a0e2f0c98ad0e9fe3cc66069509d4c2391ab74e4ecaa17d6780f4561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034000"
---
# <a name="adding-performance-counters"></a>Hinzufügen von Leistungsindikatoren

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs- und Zuverlässigkeitseinschränkungen kann die in diesem Thema beschriebene Methode zum Bereitstellen von Leistungsindikatordaten in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft, die unter [Bereitstellen von Indikatordaten mit Version 2.0](providing-counter-data-using-version-2-0.md) beschriebene Methode zum Erstellen neuer Leistungsindikatoren zu verwenden und vorhandene Leistungsindikatoren zur Verwendung dieser Methode zu migrieren.

Anwendungsspezifische Leistungsindikatoren können Ihnen helfen, die Leistung beim Entwickeln und Debuggen der Anwendung zu optimieren. Nachdem Ihre Anwendung abgeschlossen und auf Zielsystemen installiert wurde, können die Leistungsindikatoren Systemadministratoren dabei helfen, konfigurierbare Einstellungen für Ihre Anwendung anzupassen.

## <a name="adding-a-performance-object-and-its-counters"></a>Hinzufügen eines Leistungsobjekts und seiner Leistungsindikatoren

1. Entwerfen Sie die Objekttypen und Leistungsindikatoren für die Anwendung. Weitere Informationen finden Sie unter [Objekt- und Indikatorentwurf.](object-and-counter-design.md)
2. Erstellen Sie eine Initialisierungsdatei (.ini), die die Namen und Beschreibungen der von Ihnen angegebenen Leistungsobjekte und Leistungsindikatoren enthält. Weitere Informationen finden Sie unter [Hinzufügen von Indikatornamen und Beschreibungen zur Registrierung.](adding-counter-names-and-descriptions-to-the-registry.md)
3. Erstellen Sie eine Headerdatei (.h), die die relativen Offsets enthält, an denen die Indikatorobjekte und Leistungsindikatoren in der Registrierung installiert werden. Weitere Informationen finden Sie unter [Hinzufügen von Indikatornamen und Beschreibungen zur Registrierung.](adding-counter-names-and-descriptions-to-the-registry.md)
4. Richten Sie die erforderlichen Einträge für die Leistungsüberwachung in der Registrierung ein. Dies umfasst die folgenden Schritte.
    1. Erstellen Sie einen Registrierungsschlüssel im **Dienstschlüssel** für die Anwendung. Wenn Sie nicht über einen solchen Knoten verfügen, erstellen Sie ihn unter dem folgenden Registrierungsschlüssel: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Weitere Informationen finden Sie unter [Erstellen des Leistungsschlüssels der Anwendung.](creating-the-applications-performance-key.md)
    2. Verwenden Sie das Hilfsprogramm **lodctr** mit den Dateien .ini und H, um die Informationen in der Registrierung zu installieren. Dieses Hilfsprogramm ist nur erfolgreich, wenn im **Dienstschlüssel** für die Anwendung ein Leistungsschlüssel vorhanden ist. Weitere Informationen finden Sie unter [Hinzufügen von Indikatornamen und Beschreibungen zur Registrierung.](adding-counter-names-and-descriptions-to-the-registry.md)
5. Erstellen Sie eine Leistungs-DLL, die einen Satz exportierter Funktionen enthält, die dem Consumer die abgefragten Indikatordaten bereitstellen. Weitere Informationen finden Sie unter [Erstellen einer Leistungserweiterungs-DLL.](creating-a-performance-extension-dll.md)
6. Ändern Sie die Setupdatei der Anwendung, um das Hinzufügen von Informationen zur Registrierung zu automatisieren (wie in Schritt 4 beschrieben), und kopieren Sie ihre Leistungs-DLL beim Setup in das Verzeichnis Ihrer Anwendung.

Informationen zu zusätzlichen Registrierungseinträgen finden Sie unter [Creating Other Registry Entries](creating-other-registry-entries.md).
