---
description: Hinzufügen von Transformations Knoten mit topoedit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Hinzufügen von Transformations Knoten mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343768"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Hinzufügen von Transformations Knoten mit topoedit

Ein Transformations Knoten stellt eine Media Foundation Transformation (MFT) dar, die von einem Quellknoten empfangene Mediendaten verarbeitet. Wenn er bereit ist, übergibt die Pipeline ihn zum Rendern an den Ausgabe Knoten. In Media Foundation werden Encoder, Decoder, Multiplexer, de-Multiplexer und Audiovideo Effekte als MFTs implementiert. Topoedit unterstützt das Hinzufügen von Transformations Knoten, die sowohl registrierte als auch benutzerdefinierte MFTs darstellen.

Weitere Informationen zum programmgesteuerten Hinzufügen von Transformations Knoten mithilfe Media Foundation APIs finden Sie unter [Erstellen von Transformations Knoten](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>So fügen Sie der Topologie eine registrierte MFT hinzu

1.  Klicken Sie im Menü **Topologie** auf **Transformation hinzufügen**.

    Das Dialogfeld **Transformation auswählen** wird geöffnet. Es wird eine kategorisierte Liste registrierter MFTs angezeigt, die durch das Auflisten der registrierten Einträge in der Registrierung durch Aufrufen der [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion generiert wird.

2.  Erweitern Sie die Kategorie, und wählen Sie die MFT aus, die Sie der Topologie hinzufügen möchten.

3.  Klicken Sie auf **OK** , um das Dialogfeld zu schließen und zum Bereich **Topologie** zurückzukehren.

Topoedit erstellt den angegebenen Transformations Knoten. Der Bereich " **Topologie** " zeigt den Transformations Knoten als grünes Feld an, in dem der Name der MFT angezeigt wird.

## <a name="to-add-a-custom-mft-to-the-topology"></a>So fügen Sie der Topologie einen benutzerdefinierten MFT hinzu

1.  Klicken Sie im Menü **Topologie** auf **benutzerdefinierte MFT hinzufügen**.

    Dadurch wird das Dialogfeld **benutzerdefinierte GUID eingeben** geöffnet.

2.  Geben Sie im Feld **GUID:** die GUID der MFT ein, die Sie der Topologie hinzufügen möchten.

    > [!Note]  
    > Topoedit erwartet die GUID im Format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Andernfalls kann der Knoten nicht hinzugefügt werden, und es wird die Fehlermeldung "Ungültige GUID" angezeigt.

     

3.  Klicken Sie auf **OK** , um das Dialogfeld zu schließen und zum Bereich **Topologie** zurückzukehren.

Topoedit erstellt den angegebenen Transformations Knoten. Der Bereich " **Topologie** " zeigt den Transformations Knoten als grünes Feld an, in dem der Name der MFT angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Topologien mithilfe von topoedit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



