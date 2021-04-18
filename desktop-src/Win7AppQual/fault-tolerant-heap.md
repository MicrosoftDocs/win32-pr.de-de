---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Fehlertoleranter Heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352578"
---
# <a name="fault-tolerant-heap"></a>Fehlertoleranter Heap

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients:** Windows 7  

## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad:** Mittelalter  
**Häufigkeit:** Preis  


## <a name="description"></a>BESCHREIBUNG

Der Fault-tolerante Heap (Fth) ist ein Subsystem von Windows 7, das für die Überwachung von Anwendungs abstürzen und das autonome Anwenden von entschärfungen verantwortlich ist, um zukünftige Abstürze auf Anwendungs Basis zu verhindern. Bei den meisten Benutzern funktioniert Fth ohne Eingriff oder Änderung an Ihrem Teil. In einigen Fällen müssen Anwendungsentwickler und Software Tester das Standardverhalten dieses Systems jedoch möglicherweise außer Kraft setzen.

## <a name="solution"></a>Lösung

**Anzeigen der fehlertoleranten Heap Aktivität**

Der fehlertolerante Heap protokolliert Informationen, wenn der Dienst die Probleme für eine neue Anwendung startet, beendet oder damit beginnt. Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen:

1.  Klicken Sie auf das Startmenü.
2.  Klicken Sie mit der rechten Maustaste auf **Computer** , **und klicken Sie**
3.  Klicken Sie auf **Ereignisanzeige**  >  **Anwendungs-und Dienst Protokolle**  >  **Microsoft**  >  **Windows > Fault-toleranter Heap**
4.  Anzeigen von Fth-Ereignissen.

Die Dienst-und Start Ereignisse enthalten keine zusätzlichen Daten. Das Ereignis "Fth-aktiviert" enthält die Prozess-ID (PID), den Prozess Image Namen und die Startzeit der Prozess Instanz.

**Deaktivieren des fehlertoleranten Heaps**

**Vorsicht** Schwerwiegende Probleme können auftreten, wenn Sie die Registrierung falsch ändern, indem Sie den Registrierungs-Editor oder eine andere Methode verwenden. Diese Probleme müssen möglicherweise eine Neuinstallation des Betriebssystems erforderlich machen. Microsoft garantiert nicht, dass diese Probleme behoben werden können. Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.  
 Um den fehlertoleranten Heap vollständig auf einem System zu deaktivieren, legen Sie den reg \_ DWORD-Wert **HKLM \\ Software \\ Microsoft \\ Fth \\ aktiviert** auf **0** fest.

Nachdem Sie diesen Wert geändert haben, starten Sie das System neu. Fth wird für neue Anwendungen nicht mehr aktiviert.

**Zurücksetzen der Liste der von Fth verfolgten Anwendungen**

Der fehlertolerante Heap ist selbst verwalterlos und wird autonom angehalten, wenn die entschärfungen für eine bestimmte Anwendung nicht wirksam sind. Wenn Sie jedoch die Liste der Anwendungen zurücksetzen müssen, für die bei der Verwendung von Fth Probleme auftreten (z. b. Wenn Sie eine Anwendung testen und einen Absturz reproduzieren müssen, der von Fth verringert wird), können Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen:  **Rundll32.exe fthsvc.dll, fthsyspree pspezialisiert**  
**Vorsicht** Wenn Sie diesen Befehl ausführen, werden alle Fth-Anwendungen gelöscht, sodass Anwendungen, die zurzeit ordnungsgemäß funktionieren, nach dem Ausführen dieses Befehls wieder abstürzen können.  

 

 



