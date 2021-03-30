---
title: Speichern von Variablen und Typen für die Freigabe von Shadern
description: Das Klassen Verknüpfungs Objekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976824"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Speichern von Variablen und Typen für die Freigabe von Shadern

Das Klassen Verknüpfungs Objekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können. Wenn Sie ein Klassen Verknüpfungs Objekt an einen-Befehl übergeben, um einen Shader zu erstellen, sammelt die Laufzeit eine Liste der Variablen und Typen, die jede Schnittstelle im Shader implementieren können, und speichert die Namen dieser Variablen und Typen im Klassen Verknüpfungs Objekt.

Wenn Sie daher die [**ID3D11ClassLinkage:: getclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) -Methode aufrufen, um Klassen Instanzen aus dem Klassen Verknüpfungs Objekt zu generieren, kann die Common Language Runtime die Variable oder den Typ abrufen, die dem Namen entspricht, der in den einzelnen Shader bereitgestellt wird (wenn der Name für einen bestimmten Shader gültig ist) und der mit dem angegebenen Klassen Verknüpfungs Objekt erstellt wird.

Angenommen, Sie verfügen über eine einfache **Klasse, die eine** **Farb** Schnittstelle implementiert, und Sie verwenden diese Klasse in Ihrem Scheitelpunkt-Shader und PixelShader. Wenn Sie einen Shader erstellen (z. b. durch Aufrufen von [**ID3D11Device:: createpixelshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), stellt die Laufzeit fest, dass der **Light** -Klassentyp in Scheitelpunkt-und Pixel-Shadern verfügbar ist, und fügt dem Klassen Verknüpfungs Objekt den **Light** -Klassentyp hinzu. Anschließend können Sie an einem gewünschten Speicherort eine **Light** -Instanz erstellen, die Ressourcen für beide Shader binden und diese Instanz im Klassen Instanzen Array übergeben, wenn Sie den Shader auf das Gerät festlegen (z. b. durch Aufrufen von [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). Die Laufzeit führt dann die folgende Sequenz aus:

1.  Überprüft, ob die Instanz mit dem gleichen Klassen Verknüpfungs Objekt erstellt wurde.
2.  Überprüft, ob der **Light** -Klassentyp in Scheitelpunkt-und Pixel-Shadern verfügbar ist.
3.  Wählt die richtigen Funktionstabellen aus, die für den Scheitelpunkt und die Pixel-Shader unterschiedlich sein können.
4.  Sendet die Offsets, die von der-Instanz bereitstellt werden.

Das Klassen Verknüpfungs Objekt ist letztendlich ein Repository vom Typ und Variablennamen. Die maximale Anzahl von Namen, die für jedes Element (Typ und Variable) verfügbar sind, beträgt 64K. Je länger der Typ und die Variablennamen sind, desto höher ist der Speicherbedarf für die Schnittstellen Metadaten, die pro Shader gespeichert werden. Dies liegt daran, dass die Laufzeit für jeden Shader eine Zuordnung für diese Namen speichern muss.

## <a name="related-topics"></a>Verwandte Themen

[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 