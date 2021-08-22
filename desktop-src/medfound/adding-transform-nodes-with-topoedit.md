---
description: Hinzufügen von Transformationsknoten mit TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Hinzufügen von Transformationsknoten mit TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9357b08230b706dc9215cebdbc60d226cadaf0a3f1d7b29f533324ae2e3b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664930"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Hinzufügen von Transformationsknoten mit TopoEdit

Ein Transformationsknoten stellt einen Media Foundation Transform (MFT) dar, der Mediendaten verarbeitet, die er von einem Quellknoten empfängt. Wenn sie bereit ist, übergibt die Pipeline sie zum Rendern an den Ausgabeknoten. In Media Foundation werden Encoder, Decoder, Multiplexer, De-Multiplexer und Audiovideoeffekte als MFTs implementiert. TopoEdit unterstützt das Hinzufügen von Transformationsknoten, die sowohl registrierte als auch benutzerdefinierte MFTs darstellen.

Informationen zum programmgesteuerten Hinzufügen von Transformationsknoten mithilfe Media Foundation-APIs finden Sie unter [Erstellen von Transformationsknoten.](creating-transform-nodes.md)

## <a name="to-add-a-registered-mft-to-the-topology"></a>So fügen Sie der Topologie einen registrierten MFT hinzu

1.  Klicken Sie im Menü **Topologie** auf **Transformieren hinzufügen.**

    Das Dialogfeld **Transformation auswählen** wird geöffnet. Es zeigt eine kategorisierte Liste der registrierten MFTs an, die generiert wird, indem die registrierten Einträge in der Registrierung durch Aufrufen der [**MFTEnum-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) auflistet werden.

2.  Erweitern Sie die Kategorie, und wählen Sie den MFT aus, den Sie der Topologie hinzufügen möchten.

3.  Klicken Sie auf **OK,** um das Dialogfeld zu schließen und zum **Topologiebereich** zurückzukehren.

TopoEdit erstellt den angegebenen Transformationsknoten. Im **Topologiebereich** wird der Transformationsknoten als grünes Feld mit dem Namen des MFT angezeigt.

## <a name="to-add-a-custom-mft-to-the-topology"></a>So fügen Sie der Topologie einen benutzerdefinierten MFT hinzu

1.  Klicken Sie im Menü **Topologie** auf **Benutzerdefiniertes MFT hinzufügen.**

    Dadurch wird das Dialogfeld **Benutzerdefinierte GUID eingeben** geöffnet.

2.  Geben Sie im Feld **GUID:** die GUID des MFT ein, das Sie der Topologie hinzufügen möchten.

    > [!Note]  
    > TopoEdit erwartet die GUID im Format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Andernfalls kann der Knoten nicht hinzugefügt werden, und es wird die Fehlermeldung "Ungültige GUID" angezeigt.

     

3.  Klicken Sie auf **OK,** um das Dialogfeld zu schließen und zum **Topologiebereich** zurückzukehren.

TopoEdit erstellt den angegebenen Transformationsknoten. Im **Topologiebereich** wird der Transformationsknoten als grünes Feld mit dem Namen des MFT angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Topologien mit topoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



