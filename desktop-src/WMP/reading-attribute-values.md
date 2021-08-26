---
title: Lesen von Attributwerten
description: Lesen von Attributwerten
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player,Attribute für Medienelemente
- Windows Media Player Objektmodell,Attribute für Medienelemente
- Objektmodell,Attribute für Medienelemente
- Windows Media Player Mobil,Attribute für Medienelemente
- Windows Media Player ActiveX,Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement,Attribute für Medienelemente
- ActiveX,Attribute für Medienelemente
- Windows Media Player bibliothek,Attribute für Medienelemente
- Bibliothek,Attribute für Medienelemente
- Attribute,Lesen von Werten
- Lesen von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8431405b68435f41cb357a810e30c37bb96c5971824b3878b1982986aa0d0833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002830"
---
# <a name="reading-attribute-values"></a>Lesen von Attributwerten

Die Attribute, die Sie in der Bibliothek und in der Bibliothek finden, Windows Mediendateien vordefinierte Namen haben. Sie können Code schreiben, der den Wert eines Attributs abruft, indem Sie den Namen dieses Attributs an *Media übergeben.* **getItemInfo** oder *Media*. **getItemInfoByType**. Sie können auch Code schreiben, der die Werte aller Attribute in einer Datei oder einem Element abruft.

Im folgenden C#-Beispiel wird  der Wert des Title-Attributs abgerufen und in einem Meldungsfeld angezeigt. In diesem Beispiel wurde das **Player-Objekt** als axWMPLib.AxWindowsMediaPlayer Player definiert.


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



Im Aufruf von **getItemInfoByType** ist der zweite Parameter eine Zeichenfolge, die die Sprache angibt. Wenn Sie eine leere Zeichenfolge übergeben, wie in diesem Beispiel gezeigt, ruft die -Methode den Wert in der Standardsprache ab. Informationen zum dritten Parameter finden Sie unter [Attribute mit mehreren Werten.](attributes-with-multiple-values.md)

Im folgenden C#-Beispiel werden die Werte für ein bestimmtes Attribut im aktuellen Medienelement abgerufen. Diese Werte werden als durch Semikolons getrennte Zeichenfolge zurückgegeben. Beachten Sie, dass die Funktion für Attribute, die als Objekte dargestellt werden, z. B. **WM/Synchronisierung, \_** **WM/Picture** und **WM/UserWebURL,** eine leere Zeichenfolge zurückgibt.


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



Das dritte Argument, das an die **getItemInfoByType-Methode übergeben** wird, ist der Index eines bestimmten Attributs in einem Satz von Attributen mit dem gleichen Namen.

Sie können ähnlichen Code verwenden, um Attribute abzurufen, die eindeutige Namen haben. In diesen Fällen gibt **getAttributeCountByType** 1 zurück. Im zuvor gezeigten Beispiel wird der Aufruf **von getItemInfoByType** nur einmal ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern von Attributwerten**](changing-attribute-values.md)
</dt> <dt>

[**Medienelementattribute**](media-item-attributes.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten von einer CD oder DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




