---
title: Lesen von Attributwerten
description: Lesen von Attributwerten
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, Lesen von Werten
- Lesen von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339008"
---
# <a name="reading-attribute-values"></a>Lesen von Attributwerten

Die Attribute, die Sie in der Bibliothek und in Windows Media-Dateien finden, haben vordefinierte Namen. Sie können Code schreiben, der den Wert eines Attributs abruft, indem er den Namen dieses Attributs an *Medien* übergibt. **getiteminfo** oder *Medium*. **getItemInfoByType**. Sie können auch Code schreiben, der die Werte aller Attribute in einer Datei oder einem Element abruft.

Im folgenden c#-Beispiel wird der Wert des **Title** -Attributs abgerufen und in einem Meldungs Feld angezeigt. In diesem Beispiel wurde das **Player** -Objekt als AxWMPLib. AxWindowsMediaPlayer Player definiert.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



Beim Aufrufen von **getItemInfoByType** ist der zweite Parameter eine Zeichenfolge, die die Sprache angibt. Wenn Sie wie in diesem Beispiel gezeigt eine leere Zeichenfolge übergeben, ruft die-Methode den-Wert in der Standardsprache ab. Weitere Informationen zum dritten Parameter finden Sie unter [Attribute mit mehreren Werten](attributes-with-multiple-values.md).

Im folgenden c#-Beispiel werden die Werte für ein bestimmtes Attribut im aktuellen Medien Element abgerufen. Diese Werte werden als eine durch Semikolons getrennte Zeichenfolge zurückgegeben. Beachten Sie, dass bei Attributen, die als-Objekte dargestellt werden, wie z. b. **WM/ \_ liedsynchron**, **WM/Bild** und **WM/userweburl**, die-Funktion eine leere Zeichenfolge zurückgibt.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



Das dritte Argument, das an die **getItemInfoByType** -Methode übermittelt wird, ist der Index eines bestimmten Attributs in einem Attribut Satz mit demselben Namen.

Sie können ähnlichen Code verwenden, um Attribute abzurufen, die eindeutige Namen aufweisen. In diesen Fällen gibt **getattributezähltbytype** den Wert 1 zurück. Im obigen Beispiel wird der aufzurufende " **getItemInfoByType** " nur einmal ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern von Attributwerten**](changing-attribute-values.md)
</dt> <dt>

[**Medien Element Attribute**](media-item-attributes.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten von einer CD oder DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




