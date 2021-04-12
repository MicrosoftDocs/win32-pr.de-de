---
title: UI-Automatisierungs Überprüfung (UIA-Überprüfung)
description: UI Automation Verify (UIA Verify) ist ein Test Framework für manuelles und automatisiertes Testen der Implementierung von Microsoft UI Automation eines Steuer Elements oder einer Anwendung.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Benutzeroberflächenautomatisierungs-Überprüfung
- UIA-Überprüfung
- Implementierung der Benutzeroberflächen Automatisierung, testen
- Testen der Benutzeroberflächen Automatisierung
- UIA-TestTools
- Benutzeroberflächenautomatisierungs-TestTools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389956"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Barrierefreiheits Tools-UI Automation Verify (UIA Verify)

**UI Automation Verify (UIA Verify)** ist ein Test Framework für manuelles und automatisiertes Testen der Implementierung von Microsoft UI Automation eines Steuer Elements oder einer Anwendung. Die meisten Funktionen des Test Frameworks stammen aus einer DLL mit dem Namen WUIATestLibrary.dll. Diese DLL enthält den Code zum Testen spezifischer Benutzeroberflächenautomatisierungs-Funktionen und unterstützt auch die Protokollierung der Testergebnisse. Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Überprüfungen der Benutzeroberflächenautomatisierungs-Szenarios durchführen.

Die **UIA-Überprüfung** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform* > \\ uiaverify" des SDK-Installations Pfads (VisualUIAVerifyNative.exe).

Die **UIA-Überprüfung** besteht aus einer API namens Benutzeroberflächenautomatisierungs-Test Bibliothek und einer GUI-Schnittstelle namens Visual **UI Automation Verify**. Diese werden in den folgenden Themen beschrieben.

> [!NOTE]
> **Benutzeroberflächenautomatisierungs-Überprüfung** ist ein Legacy Tool. Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.

## <a name="requirements"></a>Anforderungen

Die Benutzeroberflächen Automatisierung muss auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).

**UIA Verify** wird als Teil der Gesamtmenge der Tools im Windows SDK installiert, nicht als separater Download. Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Holen Sie sich den Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)

Um die **UIA-Überprüfung** als visuelles Tool auszuführen, suchen Sie VisualUIAVerifyNative.exe im \\ Ordner "bin \\ < *Platform* > \\ uiaverify", und führen Sie Sie aus (Sie müssen in der Regel nicht als Administrator ausgeführt werden). Weitere Informationen finden Sie unter [Überprüfen der Visual UI-Automatisierung](visual-ui-automation-verify.md). Informationen zur Verwendung der Bibliotheken finden Sie unter [UI Automation Test Library](ui-automation-test-library.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
</dt> <dt>

[Überprüfen](inspect-objects.md)
</dt> <dt>

[TestTools](testing-tools.md)
</dt> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




