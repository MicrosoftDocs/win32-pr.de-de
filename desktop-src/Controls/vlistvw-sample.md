---
title: VListVW-Beispiel
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: Weitere Informationen finden Sie unter VListVW-Beispiel.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefcd39c44e79ab4eec23f7becf202d1a3cd3566f6be9496e9fd61b577c87f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957559"
---
# <a name="vlistvw-sample"></a>VListVW-Beispiel

In diesem Thema wird das VListVW-Beispielcodebeispiel beschrieben. Sie enthält die folgenden Abschnitte:

-   [Beschreibung](#description)
-   [Mindestanforderungen](#minimum-requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

Im VListVW-Beispiel wird veranschaulicht, wie sie ein einfaches virtuelles Listenansicht-Steuerelement in einer Anwendung implementieren. Ein virtuelles Listenansicht-Steuerelement ist ein Standard-Listenansicht-Steuerelement mit **dem LVS \_ OWNERDATA-Stil.** In diesem Beispiel wird ein Listenansicht-Steuerelement erstellt, das "virtuell" 100.000 Elemente enthält. Die Elemente werden nie tatsächlich hinzugefügt. Stattdessen wird dem virtuellen Listenansicht-Steuerelement mitgeteilt, wie viele Elemente es mit der [**LVM \_ SETITEMCOUNT-Meldung enthält.**](lvm-setitemcount.md) Wenn ein Element gezeichnet werden muss, fragt das Listenansichtssteuerelement das übergeordnete Fenster mit der [LVN \_ GETDISPINFO-Benachrichtigung](lvn-getdispinfo.md) nach Anzeigeinformationen ab.

## <a name="minimum-requirements"></a>Mindestanforderungen



| Produkt          | Version                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll Version 4.70             |
| Betriebssystem | Windows 95, Microsoft Windows NT 3.51 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Das VListVW-Beispiel ist auf GitHub im repository Windows [Klassische Beispiele verfügbar.](https://github.com/microsoft/Windows-classic-samples) Beispiele für Listenansichtssteuerelemente finden Sie [hier.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis.
2.  Geben Sie `msbuild [project file]` ein.

So erstellen Sie das Beispiel mithilfe Visual Studio:

1.  Öffnen Windows Explorer, und navigieren Sie zum Projektverzeichnis.
2.  Doppelklicken Sie auf das Symbol für die VCPROJ-Datei, um das Projekt in Visual Studio.
3.  Wählen Sie **im Menü Erstellen** die Option **Projektmappe erstellen aus,** um die Projektmappe zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen List-View Steuerelementen](list-view-controls-overview.md)
</dt> </dl>

 

 




