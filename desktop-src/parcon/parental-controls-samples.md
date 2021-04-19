---
description: Beispiele für Eltern Steuerelemente
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Beispiele für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352474"
---
# <a name="parental-controls-samples"></a>Beispiele für Eltern Steuerelemente

Beispielcode für die Jugendschutz Steuerelemente finden Sie unter Pfad <installation directory> \\ Windows \\ <version number> \\ Samples \\ \\ samentalcontrols. Die Beispiele lauten wie folgt:

## <a name="utilities"></a>Versorgungsunternehmen

Hilfsfunktionen für grundlegende com-Verwaltung, sid-Zeichen folgen Vorgänge und WMI-Lese-und Schreibfunktionen. Alle anderen Beispiele sind von diesem Projekt abhängig, sofern nicht anders angegeben.

## <a name="complianceapi"></a>Complianceapi

Befehlszeilen gesteuerte Konsolenanwendung, die zeigt, wie die Kompatibilitäts-API verwendet wird, um eine Schlüssel Teilmenge von Einstellungen für einen Benutzer abzurufen.

## <a name="complianceapp"></a>Complianceapp

Einfache Konsolenanwendung, die die Verwendung der Konformitäts-API veranschaulicht, um die Protokollierung erforderlicher und spezifischer Einschränkungen zu prüfen. Wenn Zeitbeschränkungen aktiviert sind, wartet die Anwendung auch auf die bevorstehenden Abmelde-Ereignisse.

## <a name="uiextensibility"></a>Uiextensibility

Befehlszeilen gesteuerte Konsolenanwendung, die die Verwendung der WMI-APIs und des WPC-Schemas veranschaulicht, um Verknüpfungen von Benutzeroberflächen-Erweiterbarkeit aufzulisten, abzufragen, hinzuzufügen, zu ändern und zu löschen.

Beispiel Befehlszeile für Beispiel:

"D: \\ WPC \\ - \\ Beispiele \\ sicherheitsparametrialcontrols \\ uiextensibility \\ Debug \\ uiextensibility" Add/g: {FD59BB7F-54AB-11dB-9666-00E08161165F}/c: 0/n: D:/WPC/Samples/Security/bientalcontrols/uiextrc/Debug/UiExtRC.dll,-101/s: d:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-103/i: d:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-104/d: D:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe

Dabei ist uiextrc eine einfache Ressourcen-DLL mit Zeichen folgen Ressourcen für die 101-und 103-ID und rund 32 um die Uhr mit Alpha Bitmaps für die Ressourcen 104 und 106.

## <a name="webextensibility"></a>Webextensibility

Eine Befehlszeilen gesteuerte Konsolenanwendung, die zeigt, wie die WMI-APIs und das WPC-Schema zum Auflisten, hinzufügen und Löschen von http-Anwendungs-oder URL-Ausnahme Einträgen und zum Festlegen und Zurücksetzen eines Webinhalts Filters mit den Eigenschaften filterid und Filter Name verwendet werden.

Der Zugriff auf die schreibgeschützten http-Anwendungs-und URL-Ausnahme Listen wird nicht angezeigt, aber der Code zum Lesen der Listen ist mit dem des Lese-/schreibfalls identisch, mit Ausnahme der Änderung des WMI-Parameters.

 

 



