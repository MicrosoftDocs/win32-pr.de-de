---
description: Leistungsindikatoren, die für Ihre Anwendung spezifisch sind, können Sie beim entwickeln und Debuggen der Anwendung unterstützen.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Hinzufügen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8660af9406de4dedec3ecbd76169a23b342aa7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358900"
---
# <a name="adding-performance-counters"></a>Hinzufügen von Leistungsindikatoren

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar. Stattdessen empfiehlt Microsoft die Verwendung der Methode, die unter [Bereitstellen von Indikator Daten mithilfe von Version 2,0](providing-counter-data-using-version-2-0.md) zum Erstellen neuer Leistungsindikatoren beschrieben wird. Außerdem empfiehlt es sich, vorhandene Leistungsindikatoren zu migrieren, um auch diese Methode zu verwenden.

Leistungsindikatoren, die für Ihre Anwendung spezifisch sind, können Sie beim entwickeln und Debuggen der Anwendung unterstützen. Nachdem die Anwendung fertiggestellt und auf Zielsystemen installiert wurde, können die Leistungsindikatoren Systemadministratoren helfen, konfigurierbare Einstellungen für Ihre Anwendung anzupassen.

## <a name="adding-a-performance-object-and-its-counters"></a>Hinzufügen eines Leistungsobjekts und seiner Leistungsindikatoren

1. Entwerfen Sie die Objekttypen und Leistungsindikatoren für die Anwendung. Weitere Informationen finden Sie unter [Object and Counter Design](object-and-counter-design.md).
2. Erstellen Sie eine Initialisierungsdatei (. ini), die die Namen und Beschreibungen der Leistungs Objekte und Leistungsindikatoren enthält, die Sie bereitstellen. Weitere Informationen finden [Sie unter Hinzufügen von Namen und Beschreibungen zur Registrierung in der Registrierung](adding-counter-names-and-descriptions-to-the-registry.md).
3. Erstellen Sie eine Header Datei (. h), die die relativen Offsets enthält, bei denen die Zähler Objekte und-Indikatoren in der Registrierung installiert werden. Weitere Informationen finden [Sie unter Hinzufügen von Namen und Beschreibungen zur Registrierung in der Registrierung](adding-counter-names-and-descriptions-to-the-registry.md).
4. Richten Sie die erforderlichen Einträge für die Leistungsüberwachung in der Registrierung ein. Dies umfasst die folgenden Schritte:
    1. Erstellen Sie im **Dienst** Schlüssel für die Anwendung einen Registrierungsschlüssel. Wenn Sie nicht über einen solchen Knoten verfügen, erstellen Sie ihn unter dem folgenden Registrierungsschlüssel: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Weitere Informationen finden Sie unter [Erstellen des Leistungs Schlüssels der Anwendung](creating-the-applications-performance-key.md).
    2. Verwenden Sie das Hilfsprogramm **Lodctr** mit den Dateien. ini und. h, um die Informationen in der Registrierung zu installieren. Dieses Hilfsprogramm ist nur erfolgreich, wenn ein Leistungs Schlüssel im **Dienst** Schlüssel für die Anwendung vorhanden ist. Weitere Informationen finden [Sie unter Hinzufügen von Namen und Beschreibungen zur Registrierung in der Registrierung](adding-counter-names-and-descriptions-to-the-registry.md).
5. Erstellen Sie eine Leistungs-DLL, die einen Satz exportierter Funktionen enthält, die die abgefragten Leistungsdaten für den Consumer bereitstellen. Weitere Informationen finden Sie unter [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md).
6. Ändern Sie die Setup Datei der Anwendung, um das Hinzufügen von Informationen zur Registrierung zu automatisieren (wie in Schritt 4 beschrieben), und kopieren Sie die Leistungs-DLL beim Setup in das Verzeichnis Ihrer Anwendung.

Weitere Informationen zu weiteren Registrierungs Einträgen finden Sie unter [Erstellen anderer Registrierungseinträge](creating-other-registry-entries.md).
