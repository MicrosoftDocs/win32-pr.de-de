---
description: 'Die Seiten des virtuellen Adressraums eines Prozesses können einen der folgenden Zustände aufweisen:'
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Seiten Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218679"
---
# <a name="page-state"></a>Seiten Status

Die Seiten des virtuellen Adressraums eines Prozesses können einen der folgenden Zustände aufweisen:



| State     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kostenlos      | Die Seite ist weder ein Commit noch reserviert. Der Prozess kann nicht auf die Seite zugreifen. Sie kann reserviert, committet oder gleichzeitig reserviert und committet werden. Der Versuch, eine freie Seite zu lesen oder auf diese zu schreiben, führt zu einer Zugriffs Verletzungs Ausnahme. <br/> Ein Prozess kann die [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) -oder [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) -Funktion verwenden, um reservierte oder zugesicherte Seiten des Adressraums freizugeben und Sie in den freien Status zurückzukehren.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reserviert  | Die Seite wurde für die zukünftige Verwendung reserviert. Der Adressbereich kann nicht von anderen Zuordnungs Funktionen verwendet werden. Auf die Seite kann nicht zugegriffen werden, und ihr ist kein physischer Speicher zugeordnet. Für den Commit ist ein Commit verfügbar. <br/> Ein Prozess kann die [**virtualzuzuordnungsfunktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder die [**virtualzuordcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) -Funktion verwenden, um Seiten des Adressraums zu reservieren, und später zum Commit der reservierten Seiten. Sie kann [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) oder [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) verwenden, um Commit-Seiten zu übernehmen und Sie in den reservierten Zustand zurückzukehren.<br/>                                                                                                                                                                                                                          |
| Committet | Arbeitsspeicher Gebühren wurden von der Gesamtgröße des RAM und von Auslagerungs Dateien auf dem Datenträger belegt. Auf die Seite kann zugegriffen werden, und der Zugriff wird von einer der [Speicherschutz Konstanten](memory-protection-constants.md)gesteuert. Das System initialisiert und lädt jede zugesicherte Seite nur während des ersten Lese-oder Schreibzugriffs auf diese Seite in den physischen Speicher. Wenn der Prozess beendet wird, gibt das System den Speicher für zugesicherte Seiten frei. <br/> Von einem Prozess kann [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**virtualzuordcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) zum Commit physischer Seiten aus einer reservierten Region verwendet werden. Außerdem können Sie Seiten gleichzeitig reservieren und Commit durchsetzen.<br/> Mit den Funktionen [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) werden zugesicherte Seiten mit Lese-/Schreibzugriff zugewiesen.<br/> |



 

 

 
