---
title: Benutzeroberflächenautomatisierung
description: Microsoft UI Automation ist ein Barrierefreiheits Framework, mit dem Windows-Anwendungen programmgesteuerte Informationen zu Benutzeroberflächen (User Interface, UIs) bereitstellen und nutzen können.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858378"
---
# <a name="ui-automation"></a>Benutzeroberflächenautomatisierung

Microsoft UI Automation ist ein Barrierefreiheits Framework, mit dem Windows-Anwendungen programmgesteuerte Informationen zu Benutzeroberflächen (User Interface, UIs) bereitstellen und nutzen können. Sie ermöglicht programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop. Sie ermöglicht Hilfstechnologieprodukten, wie z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Endbenutzer bereitzustellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben zu bearbeiten. Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.

-   [Ggf.](#where-applicable)
-   [Entwickler Zielgruppe](#developer-audience)
-   [Lauf Zeitanforderungen](#run-time-requirements)
-   [Unterstützung für Betriebssysteme mit Unterstützung](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Anwendbarkeit

Durch die Verwendung der Benutzeroberflächen Automatisierung und der folgenden Barrierefreiheits Funktionen können Entwickler Anwendungen, die auf Windows ausgeführt werden, für viele Personen mit Sehbehinderung, Hörbehinderungen oder Bewegungsbehinderungen leichter zugänglich machen. Außerdem ist die Benutzeroberflächen Automatisierung speziell für die Bereitstellung robuster Funktionen für automatisierte Testszenarien konzipiert.

## <a name="developer-audience"></a>Entwicklerzielgruppe

Die Benutzeroberflächen Automatisierung wurde für erfahrene C/C++-Entwickler entwickelt. Im Allgemeinen benötigen Entwickler einen mittleren Einblick in die Component Object Model (com)-Objekte und-Schnittstellen, die Unicode-und die Windows-API-Programmierung.

Weitere Informationen zur Benutzeroberflächen Automatisierung für verwalteten Code finden Sie im MSDN-Abschnitt .NET Framework Developer es Guide ( [Barrierefreiheit](/dotnet/framework/ui-automation/) ).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Automatisierung der Benutzeroberfläche wird unter den folgenden Betriebssystemen unterstützt: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 und Windows Server 2019.

> [!Note]  
> Windows XP und Windows Server 2003 benötigen auch Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Unterstützung für Betriebssysteme mit Unterstützung

Das Platt Form Update für Windows Vista ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen sowohl auf Windows 7 als auch auf Betriebssysteme von Windows 7 als Ziel festzulegen. Das Platt Form Update für Windows Server 2008 ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen sowohl auf Windows Server 2008 R2 als auch auf frühere Versionen von Windows Server zu aktualisieren. Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein. Anwendungen von Drittanbietern, die ein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 erfordern, können Windows Update erkennen, ob es installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 unterstützen beide das gesamte Feature "Windows Automation API 3,0", das auf den folgenden Betriebssystemen festgelegt ist.

-   Windows XP (Englisch) <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 und x64)  
    </dl>
-   Windows Vista (Englisch) <dl> Starter SP2 (x86 und x64)  
    Home Premium SP2 (x86 und x64)  
    Business SP2 (x86 und x64)  
    Enterprise SP2 (x86 und x64)  
    Ultimate SP2 (x86 und x64)  
    </dl>
-   Windows Server 2008 (Englisch) <dl> Windows Server 2008 SP2 (x86 und x64)  
    </dl>

Weitere Informationen zu beiden Updates finden Sie unter [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
-   [Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md)
-   [Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch](uiauto-clientportal.md)
-   [Verweis](entry-uiautocore-ref.md)
-   [Beispiele](samples-entry.md)
-   [Anhänge](appendix-entry.md)

 

 