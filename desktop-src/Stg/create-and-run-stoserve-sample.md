---
title: Beispiel zum Erstellen und Ausführen von stoservice
description: Das Client Beispiel und andere verwandte Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341440"
---
# <a name="create-and-run-stoserve-sample"></a>Beispiel zum Erstellen und Ausführen von stoservice

Das Client Beispiel und andere verwandte Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können. Weitere Informationen zum Erstellen der Beispiele finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md). Wenn Sie bereits die entsprechenden Beispiele erstellt haben, ist STOCLIEN.EXE die ausführbare Client Datei, die für das **stoservice** -Beispiel ausgeführt werden soll.

## <a name="code-tour"></a>Codetour

In der folgenden Tabelle sind die für das **stoservice** -Beispiel relevanten Dateien aufgeführt.



| Dateien        | BESCHREIBUNG                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | Kurze Beispiel Beschreibung                                                                                                  |
| Makefile     | Das generische Makefile zum Entwickeln des STOSERVE.DLL Code Beispiels für diese Lektion.                                            |
| Stoservice. Micha   | Die Includedatei zum Deklarieren als importiert oder definiert als exportierter Dienstfunktionen in STOSERVE.DLL.                 |
| Stoservice. CPP | Die Haupt Implementierungs Datei für STOSERVE.DLL. Verfügt über die DllMain-und die com-Serverfunktionen (z. b. DllGetClassObject). |
| Stoservice. Auflösenden | Die Modul Definitionsdatei. Exportiert Server-Wohnfunktionen.                                                             |
| Stoservice. RC  | Die dll-Ressourcen Definitionsdatei für die ausführbare Datei.                                                                      |
| Stoservice. ICO | Die Symbol Ressource für die ausführbare Datei.                                                                                     |
| Servers. Micha     | Die Includedatei für das Server Steuerelement C++-Objekt.                                                                       |
| Servers. CPP   | Die Implementierungs Datei für das Server Steuerelement C++-Objekt.                                                                |
| Schen. Micha    | Die Includedatei für die Klassenfactory-com-Objekte des Servers.                                                              |
| Schen. CPP  | Die Implementierungs Datei für die Klassenfactorys des Servers.                                                                 |
| Herzustellen. Micha    | Die Includedatei für den Verbindungspunkt-Enumerator, den Verbindungspunkt und die Verbindungs Enumeratorklassen.                |
| Herzustellen. CPP  | Die Implementierungs Datei für den Verbindungspunkt-Enumerator, den Verbindungspunkt und die Verbindungs Enumeratorobjekte.         |
| Zeitung. Micha      | Die Includedatei für die copaper-com-Objektklasse.                                                                        |
| Zeitung. CPP    | Die Implementierungs Datei für die copaper-com-Objektklasse und die Verbindungspunkte.                                       |
| Stoservice. DSP | Microsoft Visual Studio Projektdatei.                                                                                     |



 

Die wichtigsten Themen, die in dieser codetour behandelt werden, sind:

-   Die [**iPaper**](ipaper-methods.md) -Schnittstellen Methoden.
-   Verwendung der [**ipapersink**](ipapersink-methods.md) -Schnittstelle für Client Benachrichtigungen durch copaper.
-   [**Strukturen**](structures---stoserve.md) in stoservice.
-   [Überlegungen zu Unicode](unicode-considerations.md).

 

 




