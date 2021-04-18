---
title: Vlistvw-Beispiel
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: Weitere Informationen zu vlistvw Sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344217"
---
# <a name="vlistvw-sample"></a>Vlistvw-Beispiel

In diesem Thema wird das Beispielcode Beispiel für vlistvw beschrieben. Sie enthält die folgenden Abschnitte:

-   [Beschreibung](#description)
-   [Mindestanforderungen](#minimum-requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

Das vlistvw-Beispiel zeigt, wie ein einfaches virtuelles Listenansicht-Steuerelement in einer Anwendung implementiert wird. Ein virtuelles Listenansicht-Steuerelement ist ein Standardmäßiges Listenansicht-Steuerelement mit dem **LVS-Besitzer \_ Daten** Stil. In diesem Beispiel wird ein Listenansicht-Steuerelement erstellt, das "virtuell" 100.000 Elemente enthält. Die Elemente werden nie tatsächlich hinzugefügt. Stattdessen wird das Steuerelement [**für die virtuelle \_**](lvm-setitemcount.md) Listenansicht "erzählt", wie viele Elemente es enthält. Wenn ein Element gezeichnet werden muss, fragt das Listenansicht-Steuerelement das übergeordnete Fenster nach Anzeigeinformationen mit der [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigung ab.

## <a name="minimum-requirements"></a>Mindestanforderungen



| Produkt          | Version                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll Version 4,70             |
| Betriebssystem | Windows 95, Microsoft Windows NT 3,51 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Das vlistvw-Beispiel ist auf GitHub im [klassischen Windows-beispielrepository](https://github.com/microsoft/Windows-classic-samples)verfügbar. Die Listenansicht-Steuerelement Elemente finden Sie [hier](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw) .

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis.
2.  Geben Sie `msbuild [project file]` ein.

So erstellen Sie das Beispiel mithilfe von Visual Studio:

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.
2.  Doppelklicken Sie auf das Symbol für die VCPROJ-Datei, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> </dl>

 

 




