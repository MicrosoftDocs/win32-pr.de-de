---
title: Speichern von Variablen und Typen für die Freigabe von Shadern
description: Das Klassenverknüpfungsobjekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam verwendet werden können.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d40526274ea52d68b0a02dbefd02c116ded77d64e8b343a48abef2735446d971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853170"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Speichern von Variablen und Typen für die Freigabe von Shadern

Das Klassenverknüpfungsobjekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam verwendet werden können. Wenn Sie ein Klassenverknüpfungsobjekt in einem Aufruf zum Erstellen eines Shaders übergeben, sammelt die Laufzeit eine Liste von Variablen und Typen, die jede Schnittstelle im Shader implementieren können, und speichert die Namen dieser Variablen und Typen im Klassenverknüpfungsobjekt.

Wenn Sie daher die [**ID3D11ClassLinkage::GetClassInstance-Methode**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) aufrufen, um Klasseninstanzen aus dem Klassenverknüpfungsobjekt zu generieren, kann die Laufzeit die Variable oder den Typ abrufen, die dem Namen entspricht, der in jedem Shader angegeben ist (wenn dieser Name für einen bestimmten Shader gültig ist) und der mit dem angegebenen Klassenverknüpfungsobjekt erstellt wird.

Angenommen, Sie verfügen  über eine Light-Klasse, die eine **Color-Schnittstelle** implementiert, und Sie verwenden diese Klasse in Ihrem Vertex-Shader und Pixel-Shader. Wenn Sie einen Shader erstellen (z. B. durch Aufrufen von [**ID3D11Device::CreatePixelShader),**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)bestimmt die Runtime, dass der **Light-Klassentyp** sowohl in Vertex- als auch in Pixelshadern verfügbar ist, und fügt dem Klassenverknüpfungsobjekt den **Light-Klassentyp** hinzu. Sie können dann eine **Light-Instanz** an einem speicherort erstellen, an den Sie möchten, die Ressourcen für beide Shader binden und diese Instanz im Klasseninstanzarray übergeben, wenn Sie den Shader auf das Gerät festlegen (z. B. durch Aufrufen von [**ID3D11DeviceContext::P SSetShader).**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader) Die Runtime führt dann die folgende Sequenz aus:

1.  Überprüft, ob die Instanz mit demselben Klassenverknüpfungsobjekt erstellt wurde.
2.  Überprüft, ob der **Light-Klassentyp** sowohl in Vertex- als auch in Pixel-Shadern verfügbar ist.
3.  Wählt die richtigen Funktionstabellen aus, die sich für vertex- und pixel-Shader unterscheiden können.
4.  Sendet die offsets, die die -Instanz bietet, nach unten.

Das Klassenverknüpfungsobjekt ist letztendlich ein Repository mit Typ- und Variablennamen. Die maximale Anzahl von Namen, die für jedes Element (Typ und Variable) verfügbar sind, beträgt 64.000. Je länger die Typ- und Variablennamen sind, desto höher ist die Speicheranforderung für die Schnittstellenmetadaten, die pro Shader gespeichert werden. Dies liegt daran, dass die Runtime eine Zuordnung für diese Namen für jeden Shader speichern muss.

## <a name="related-topics"></a>Verwandte Themen

[Dynamische Verknüpfung](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Verknüpfung](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 