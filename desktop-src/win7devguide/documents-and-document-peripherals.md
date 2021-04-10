---
title: Dokumente und Dokument Peripheriegeräte
description: Windows 7 bietet Entwicklern eine robuste Plattform zum Arbeiten mit Dokumenten und zum Integrieren von Dokument Peripheriegeräten.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039393"
---
# <a name="documents-and-document-peripherals"></a>Dokumente und Dokument Peripheriegeräte

Windows 7 bietet Entwicklern eine robuste Plattform zum Arbeiten mit Dokumenten und zum Integrieren von Dokument Peripheriegeräten. In Windows Vista wurden zwei neue Dokument-und Speichertechnologien eingeführt: XML Paper Specification (XPS) und Open Packaging Conventions (OPC). Diese Technologien, die nur für Entwickler von Anwendungen mit verwaltetem Code über das Microsoft .NET Framework in Windows Vista verfügbar waren, stehen nun im Windows 7 Software Development Kit (SDK) zur Verfügung, die von Entwicklern von nicht verwaltetem Code verwendet werden können.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

Windows 7 unterstützt alle OPC-Dateiformate, einschließlich derjenigen von Microsoft und von Drittanbietern. OPC ist eine Komponente der internationalen Office Open XML (OOXML)-Spezifikation, die über *ISO/IEC DIS 29500* und *ECMA-376* definiert ist. Auf Grundlage des *ZIP* -Datei Formats ermöglicht OPC Anwendungen, eine Kombination von Datenelementen in einer einzelnen Paketdatei zu speichern. Anwendungsentwickler können die *Paket*-APIs in Windows 7 verwenden, um mehrere Datenelemente in OPC-basierten Dateien zu erstellen, zu lesen und zu bearbeiten.

Mithilfe der *Pack*-APIs in Windows 7 können Entwickler neue Paketformate erstellen, um anwendungsspezifische Daten Speicherungs Anforderungen zu erfüllen.

Digitale *X509* -Signaturen werden auch von den *Paket*-APIs unterstützt. Entwickler können die Funktionen für digitale Signaturen verwenden, um ausgewählte Teile eines OPC-Pakets oder das gesamte Paket zu signieren und zu überprüfen. Anwendungen können Ihren Dokumenten eine zusätzliche Sicherheitsstufe zur Verfügung stellen, indem Sie digitale Signaturen verwenden, um zu erkennen, wann der Inhalt einer OPC-basierten Datei geändert wurde, nachdem die Datei signiert wurde. (Siehe [Übersicht über die Open Packaging-Konventionen](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview).)

## <a name="xps-documents"></a>XPS-Dokumente

Entwickler von Windows-Anwendungen können Anwendungen erstellen, die XPS-Dokumente mit Windows 7 erstellen. Dies ermöglicht es Ihnen, eng in das Ökosystem der Dokument Peripherie (Geräte wie Scanner und Drucker) zu integrieren und mit einem sicheren elektronischen Papier zu arbeiten, um die Veröffentlichung und Archivierung zu unterstützen.

In früheren Versionen von Windows wurde XPS für Microsoft Win32-Entwickler nicht unterstützt. XPS wurde in Windows Vista eingeführt, aber die API-Oberfläche war auf .NET-Entwickler beschränkt, die mit verwaltetem Code arbeiten. Mit Windows 7 können Win32-Entwickler die neuen XPS-*Dokument*-APIs verwenden, um den Arbeitsaufwand zu reduzieren, der bei der Arbeit mit XPS erforderlich ist. Da XPS die Grundlage für die neue Windows-Druck Plattform ist, ist dies ein bedeutender Vorteil.

In früheren Versionen von Windows war der Zugriff auf den XPS-Druckpfad von Win32-Anwendungen auf Treiber Escapezeichen beschränkt. Dadurch wurde der Druck Pfad für Entwickler, die keinen verwalteten Code verwenden, erheblich reduziert. Für Win32-Entwickler reduziert die neue XPS-*Druck*-API erheblich den Aufwand, der erforderlich ist, um von den Vorteilen des XPS-Druck Pfads zu profitieren, und es entfällt die Notwendigkeit von parallelem Druck Code.

Anwendungsentwickler können XPS-Dokumente verwenden, um Inhalte als elektronisches Papier in einem High-Fidelity-, effizienten und vertrauenswürdigen Format freizugeben und zu archivieren. Genau wie bei Windows Vista basiert der Druckpfad in Windows 7 auf dem XPS-Format, um erweiterte Druckfunktionen bereitzustellen. Die XPS-Dokument-APIs in Windows 7 erleichtern Entwicklern das Erstellen, zugreifen auf und Bearbeiten von XPS-Dokumenten. (Siehe [XPS-Programmier Handbuch für Dokumente](/previous-versions//dd372978(v=vs.85)).)

![XPS-Viewer](images/windows7-devguide-xpsviewer.jpg)

Entwickler von Windows-Anwendungen können Anwendungen erstellen, die XPS-Dokumente mit Windows 7 erstellen.

 

 