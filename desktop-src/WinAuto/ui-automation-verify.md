---
title: Benutzeroberflächenautomatisierung Überprüfen (UIA-Überprüfung)
description: Benutzeroberflächenautomatisierung Verify (UIA Verify) ist ein Testframework zum manuellen und automatisierten Testen der Implementierung eines Steuerelements oder einer Anwendung von Microsoft Benutzeroberflächenautomatisierung.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Benutzeroberflächenautomatisierungs-Überprüfung
- UIA-Überprüfung
- Benutzeroberflächenautomatisierung Implementierung,Testen
- Testen Benutzeroberflächenautomatisierung
- UIA-Testtools
- Benutzeroberflächenautomatisierung Von Testtools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f8c97d6522e353445ededff47a9a7cf123998b94f1323f1df59b7a380ac1d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052388"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Barrierefreiheitstools – Benutzeroberflächenautomatisierung Überprüfen (UIA-Überprüfung)

**Benutzeroberflächenautomatisierung Verify (UIA Verify)** ist ein Testframework zum manuellen und automatisierten Testen der Implementierung eines Steuerelements oder einer Anwendung von Microsoft Benutzeroberflächenautomatisierung. Die meisten Funktionen des Testframeworks stammen aus einer DLL namens WUIATestLibrary.dll. Diese DLL enthält den Code zum Testen bestimmter Benutzeroberflächenautomatisierung Funktionen und unterstützt auch die Protokollierung der Testergebnisse. Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Spot-Überprüfungen Ihrer Benutzeroberflächenautomatisierung Szenarien durchführen.

**Die UIA-Überprüfung** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner bin \\ < *version* > \\ < *platform* > \\ UIAVerify des SDK-Installationspfads (VisualUIAVerifyNative.exe).

**UIA Verify** besteht aus einer API namens Benutzeroberflächenautomatisierung Test Library und einer GUI-Schnittstelle namens Visual **Benutzeroberflächenautomatisierung Verify**. Diese werden in den folgenden Themen beschrieben.

> [!NOTE]
> **Benutzeroberflächenautomatisierung Verify** ist ein Legacytool. Es wird empfohlen, stattdessen [Barrierefreiheit Insights](https://accessibilityinsights.io/) zu verwenden.

## <a name="requirements"></a>Anforderungen

Benutzeroberflächenautomatisierung müssen auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md).

**UIA Verify** wird als Teil des gesamten Toolssatzes im Windows SDK installiert und nicht als separater Download verteilt. Das Windows SDK enthält alle tools im Zusammenhang mit der Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Abrufen des Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Downloadarchiv, das von dieser Seite verknüpft ist, wenn Sie eine frühere Version benötigen.)

Um **UIA Verify** als visuelles Tool auszuführen, suchen Sie VisualUIAVerifyNative.exe im \\ Ordner \\ < "bin *platform* > \\ UIAVerify", und führen Sie ihn aus (sie müssen in der Regel nicht als Administrator ausgeführt werden). Weitere Informationen finden Sie unter [Visual Benutzeroberflächenautomatisierung Verify](visual-ui-automation-verify.md). Informationen zur Verwendung der Bibliotheken finden Sie unter [Benutzeroberflächenautomatisierung Testbibliothek.](ui-automation-test-library.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
</dt> <dt>

[Überprüfen](inspect-objects.md)
</dt> <dt>

[Testtools](testing-tools.md)
</dt> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




