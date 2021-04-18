---
description: Ihre Direct3D-Anwendung kann jedem Scheitelpunkt eines primitiven Texturkoordinaten zuweisen.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Textur Adressierungs Modi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ebad5fdb141c41c43c651a2188640d7a6b764e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339673"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Textur Adressierungs Modi (Direct3D 9)

Ihre Direct3D-Anwendung kann jedem Scheitelpunkt eines primitiven Texturkoordinaten zuweisen. Weitere Informationen finden Sie unter [Texturkoordinaten (Direct3D 9)](texture-coordinates.md). Die u-und v-Texturkoordinaten, die Sie einem Scheitelpunkt zuweisen, liegen in der Regel im Bereich von 0,0 bis 1,0. Wenn Sie jedoch Texturkoordinaten außerhalb dieses Bereichs zuweisen, können Sie bestimmte besondere texturierungseffekte erstellen.

Sie steuern, was Direct3D mit Texturkoordinaten bewirkt, die außerhalb des \[ Bereichs von 0,0, 1,0 liegen, \] indem Sie den Textur Adressierungs Modus festlegen. Beispielsweise können Sie festlegen, dass die Anwendung den Textur Adressierungs Modus so festlegen soll, dass eine Textur über eine primitive Kachel verteilt wird.

Direct3D ermöglicht Anwendungen das Durchführen von Textur Umbrüchen. Es ist wichtig zu beachten, dass das Festlegen des Textur Adressierungs Modus auf D3DTADDRESS \_ Wrap nicht mit dem Durchführen von Textur Umbrüche identisch ist. Wenn der Textur Adressierungs Modus auf D3DTADDRESS Wrap festgelegt \_ wird, werden mehrere Kopien der Quell Textur auf den aktuellen primitiven angewendet, und durch das Aktivieren von Textur Umbruch ändert sich die Art und Weise, wie das System strukturierte Polygone raiert. Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).

Durch das Aktivieren von Textur Wrapping werden Texturkoordinaten effektiv außerhalb des \[ 0,0-, 1,0 \] -Bereichs ungültig, und das Verhalten bei der rasterisierung solcher delinquente Texturkoordinaten ist in diesem Fall nicht definiert. Wenn Textur Wrapping aktiviert ist, werden keine Textur Adressierungs Modi verwendet. Achten Sie darauf, dass Ihre Anwendung keine Texturkoordinaten angibt, die kleiner als 0,0 oder größer als 1,0 sind, wenn die Textur Umschreibung aktiviert ist.

## <a name="setting-the-addressing-mode"></a>Festlegen des Adressierungs Modus

Sie können die Textur Adressierungs Modi für einzelne Textur Stufen festlegen, indem Sie die [**IDirect3DDevice9:: setsamplerstate**](/windows/desktop/api) -Methode aufrufen. Geben Sie den gewünschten Textur Stufen Bezeichner im *Sampler* -Parameter an. Legen Sie den *Typparameter* auf D3DSAMP \_ adressu, D3DSAMP \_ adressvc oder D3DSAMP \_ AddressW fest, um die u-, v-oder w-Adressierungs Modi einzeln zu aktualisieren. Der *value* -Parameter bestimmt, welcher Modus festgelegt wird. Dies kann ein beliebiger Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps sein. Um den aktuellen Textur Adress Modus für eine Textur Phase abzurufen, rufen Sie [**IDirect3DDevice9:: getsamplerstate**](/windows/desktop/api)auf, indem Sie die D3DSAMP \_ adressssu-, D3DSAMP \_ addressvc-oder D3DSAMP \_ AddressW-Member der [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) -Enumeration verwenden, um den Adress Modus zu identifizieren, über den Sie Informationen erhalten möchten.

## <a name="device-limitations"></a>Geräte Einschränkungen

Obwohl das System im allgemeinen Texturkoordinaten außerhalb des Bereichs von 0,0 und 1,0 (einschließlich) zulässt, beeinflussen Hardware Einschränkungen häufig, wie weit außerhalb der Bereichs Texturkoordinaten liegen kann. Ein renderinggerät kommuniziert dieses Limit im **MaxTextureRepeat** -Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, wenn Sie Gerätefunktionen abrufen. Der Wert in diesem Member beschreibt den vollständigen Bereich der Texturkoordinaten, die vom Gerät zugelassen werden. Wenn dieser Wert beispielsweise 128 ist, müssen die Eingabe Texturkoordinaten im Bereich von-128,0 bis + 128,0 beibehalten werden. Das übergeben von Vertices mit Texturkoordinaten außerhalb dieses Bereichs ist ungültig. Die gleiche Einschränkung gilt für die Texturkoordinaten, die als Ergebnis der automatischen Texturkoordinaten Generierung und der Texturkoordinaten Transformationen generiert werden.

Die Interpretation von **maxtextureretorf** wirkt sich auch auf das D3DPTEXTURECAPS \_ texrepeatnotscaledbysize-Funktions Bit aus. Wenn dieses Bit festgelegt ist, wird der Wert im **MaxTextureRepeat** -Member genau wie beschrieben verwendet. Wenn jedoch D3DPTEXTURECAPS \_ texrepeatnotscaledbysize nicht festgelegt ist, hängen die Grenzen der Textur Wiederholung von der Größe der Textur ab, die von den Texturkoordinaten indiziert wird. In diesem Fall muss **MaxTextureRepeat** von der aktuellen Textur Größe auf der größten Detailebene skaliert werden, um den gültigen Texturkoordinaten Bereich zu berechnen. Wenn z. b. eine Textur Dimension von 32 und **maxtextureretorf** 512 ist, ist der tatsächliche gültige Texturkoordinaten Bereich 512/32 = 16, sodass sich die Texturkoordinaten für dieses Gerät im Bereich von-16,0 bis + 16,0 befinden müssen.

Weitere Informationen über die Textur Adressierungs Modi sind in den folgenden Themen enthalten.

-   [Wrap-Textur Adress Modus (Direct3D 9)](wrap-texture-address-mode.md)
-   [Spiegel Textur Adress Modus (Direct3D 9)](mirror-texture-address-mode.md)
-   [Einspannen des Textur Adress Modus (Direct3D 9)](clamp-texture-address-mode.md)
-   [Border Color Texture Address Mode (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Texturierung](basic-texturing-concepts.md)
</dt> </dl>

 

 
