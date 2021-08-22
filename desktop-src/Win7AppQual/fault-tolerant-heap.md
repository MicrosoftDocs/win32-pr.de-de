---
description: Fehlertoleranter Heap
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Fehlertoleranter Heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99d6df576906c82a3c0bc95ca4dc8b8ae54b26433c9fb213da5917d596af947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053168"
---
# <a name="fault-tolerant-heap"></a>Fehlertoleranter Heap

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients –** Windows 7  

## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Mittel  
**Häufigkeit:** Niedrig  


## <a name="description"></a>Beschreibung

Der fehlertolerante Heap (Fault Tolerant Heap, FTH) ist ein Subsystem von Windows 7, das für die Überwachung von Anwendungsabstürzen und die autonome Anwendung von Entschärfungen verantwortlich ist, um zukünftige Abstürze pro Anwendung zu verhindern. Für die überwiegende Mehrheit der Benutzer funktioniert FTH ohne Eingreifen oder Änderung. In einigen Fällen müssen Anwendungsentwickler und Softwaretester jedoch möglicherweise das Standardverhalten dieses Systems außer Kraft setzen.

## <a name="solution"></a>Lösung

**Anzeigen der Fehlertoleranten Heapaktivität**

Fehlertoleranter Heap protokolliert Informationen, wenn der Dienst gestartet, beendet oder damit beginnt, Probleme für eine neue Anwendung zu beheben. Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen:

1.  Klicken Sie auf das Startmenü.
2.  Klicken Sie mit der rechten **Maustaste auf Computer,** und klicken Sie **auf Verwalten.**
3.  Klicken **Ereignisanzeige**  >  **auf Anwendungs- und Dienstprotokolle**  >  **Microsoft**  >  **Windows > Fehlertoleranter Heap**
4.  Zeigen Sie FTH-Ereignisse an.

Die Ereignisse zum Beenden und Starten des Diensts enthalten keine zusätzlichen Daten. Das FTH Enabled-Ereignis enthält die Prozess-ID (PID), den Prozessimagenamen und die Startzeit der Prozessinstanz.

**Deaktivieren des fehlertoleranten Heaps**

**Vorsicht** Schwerwiegende Probleme können auftreten, wenn Sie die Registrierung falsch ändern, indem Sie den Registrierungs-Editor oder eine andere Methode verwenden. Diese Probleme erfordern möglicherweise, dass Sie das Betriebssystem neu installieren. Microsoft garantiert nicht, dass diese Probleme behoben werden können. Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.  
 Um den fehlertoleranten Heap vollständig auf einem System zu deaktivieren, legen Sie den REG \_ DWORD-Wert **HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** auf **0 fest.**

Starten Sie das System neu, nachdem Sie diesen Wert geändert haben. FTH wird für neue Anwendungen nicht mehr aktiviert.

**Zurücksetzen der Liste der vom FTH nachverfolgten Anwendungen**

Der fehlertolerante Heap ist selbstver- verwaltend und wird die Anwendung autonomer Weise beenden, falls Die Entschärfungen für eine bestimmte Anwendung nicht wirksam sind. Wenn Sie jedoch die Liste der Anwendungen zurücksetzen müssen, für die FTH Probleme entschädigt (z. B. wenn Sie eine Anwendung testen und einen Absturz reproduzieren müssen, der durch FTH entschädigt wird), können Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**  
**Vorsicht** Wenn Sie diesen Befehl ausführen, werden alle FTH-Anwendungen entäussert, sodass Anwendungen, die derzeit ordnungsgemäß funktionieren, nach dem Ausführen dieses Befehls möglicherweise wieder abstürzen.  

 

 



