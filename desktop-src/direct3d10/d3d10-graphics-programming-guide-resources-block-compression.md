---
description: Die Block Komprimierung ist eine Textur Komprimierungs Methode zum Reduzieren der Textur Größe.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Block Komprimierung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568236"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="3e289-103">Block Komprimierung (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3e289-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="3e289-104">Die Block Komprimierung ist eine Textur Komprimierungs Methode zum Reduzieren der Textur Größe.</span><span class="sxs-lookup"><span data-stu-id="3e289-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="3e289-105">Im Vergleich zu einer Textur mit 32 Bit pro Farbe kann eine Block komprimierte Textur bis zu 75 Prozent kleiner sein.</span><span class="sxs-lookup"><span data-stu-id="3e289-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="3e289-106">Anwendungen sehen in der Regel eine Leistungssteigerung bei der Verwendung der Block Komprimierung aufgrund der geringeren Speicher Beanspruchung.</span><span class="sxs-lookup"><span data-stu-id="3e289-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="3e289-107">Die Block Komprimierung funktioniert zwar gut, aber Sie wird für alle Texturen empfohlen, die von der Pipeline transformiert und gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="3e289-108">Texturen, die direkt dem Bildschirm zugeordnet sind (UI-Elemente wie Symbole und Text), sind keine guten Auswahlmöglichkeiten für die Komprimierung, da Artefakte leichter erkennbar sind.</span><span class="sxs-lookup"><span data-stu-id="3e289-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="3e289-109">Eine Block komprimierte Textur muss als Vielfaches der Größe 4 in allen Dimensionen erstellt werden und kann nicht als Ausgabe der Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="3e289-110">Wie funktioniert die Block Komprimierung?</span><span class="sxs-lookup"><span data-stu-id="3e289-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="3e289-111">Speichern von nicht komprimierten Daten</span><span class="sxs-lookup"><span data-stu-id="3e289-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="3e289-112">Speichern von komprimierten Daten</span><span class="sxs-lookup"><span data-stu-id="3e289-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="3e289-113">Verwenden von Block Komprimierung</span><span class="sxs-lookup"><span data-stu-id="3e289-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="3e289-114">Virtuelle Größe im Vergleich zur physischen Größe</span><span class="sxs-lookup"><span data-stu-id="3e289-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="3e289-115">Komprimierungs Algorithmen</span><span class="sxs-lookup"><span data-stu-id="3e289-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="3e289-116">BC1</span><span class="sxs-lookup"><span data-stu-id="3e289-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="3e289-117">BU2</span><span class="sxs-lookup"><span data-stu-id="3e289-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="3e289-118">BC3</span><span class="sxs-lookup"><span data-stu-id="3e289-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="3e289-119">BC4</span><span class="sxs-lookup"><span data-stu-id="3e289-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="3e289-120">BC5</span><span class="sxs-lookup"><span data-stu-id="3e289-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="3e289-121">Format Konvertierung mit Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="3e289-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="3e289-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e289-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="3e289-123">Wie funktioniert die Block Komprimierung?</span><span class="sxs-lookup"><span data-stu-id="3e289-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="3e289-124">Die Block Komprimierung ist eine Technik zum Reduzieren des Arbeitsspeichers, der zum Speichern von Farbdaten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3e289-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="3e289-125">Wenn Sie einige Farben in ihrer ursprünglichen Größe und andere Farben mithilfe eines Codierungs Schemas speichern, können Sie die Menge an Arbeitsspeicher, die zum Speichern des Bilds erforderlich ist, erheblich reduzieren.</span><span class="sxs-lookup"><span data-stu-id="3e289-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="3e289-126">Da komprimierte Daten von der Hardware automatisch decodiert werden, gibt es keine Leistungs Einbuße bei der Verwendung komprimierter Texturen.</span><span class="sxs-lookup"><span data-stu-id="3e289-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="3e289-127">Sehen Sie sich die folgenden beiden Beispiele an, um zu sehen, wie die Komprimierung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3e289-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="3e289-128">Im ersten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern von nicht komprimierten Daten verwendet wird. im zweiten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern komprimierter Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="3e289-129">Speichern von nicht komprimierten Daten</span><span class="sxs-lookup"><span data-stu-id="3e289-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="3e289-130">Die folgende Abbildung stellt eine unkomprimierte 4 × 4-Textur dar.</span><span class="sxs-lookup"><span data-stu-id="3e289-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="3e289-131">Nehmen Sie an, dass jede Farbe eine einzelne Farbkomponente (z. h. rot) enthält und in einem Byte Arbeitsspeicher gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![Abbildung einer unkomprimierten 4 x 4-Textur](images/d3d10-block-compress-1.png)

<span data-ttu-id="3e289-133">Die nicht komprimierten Daten werden sequenziell im Speicher angeordnet und erfordern 16 Bytes, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![Abbildung von nicht komprimierten Daten in sequenzieller Arbeitsspeicher](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="3e289-135">Speichern von komprimierten Daten</span><span class="sxs-lookup"><span data-stu-id="3e289-135">Storing Compressed Data</span></span>

<span data-ttu-id="3e289-136">Nachdem Sie nun gesehen haben, wie viel Arbeitsspeicher ein nicht komprimiertes Image verwendet, sehen Sie sich an, wie viel Arbeitsspeicher ein komprimiertes Image speichert.</span><span class="sxs-lookup"><span data-stu-id="3e289-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="3e289-137">Das [BC1](#bc1) -Komprimierungs Format speichert zwei Farben (jeweils 1 Byte) und 16 3-Bit-Indizes (48 Bits oder 6 Bytes), mit denen die ursprünglichen Farben in der Textur interpolieren werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![Abbildung des BC1-Komprimierungs Formats](images/d3d10-block-compress-3.png)

<span data-ttu-id="3e289-139">Der Gesamt Speicherplatz, der zum Speichern der komprimierten Daten erforderlich ist, beträgt 8 50 Byte</span><span class="sxs-lookup"><span data-stu-id="3e289-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="3e289-140">Die Einsparungen sind noch größer, wenn mehr als eine Farbkomponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="3e289-141">Die beträchtlichen Speicher Einsparungen durch die Block Komprimierung können zu einer Leistungssteigerung führen.</span><span class="sxs-lookup"><span data-stu-id="3e289-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="3e289-142">Diese Leistung ergibt sich aus den Kosten der Bildqualität (aufgrund der Farb interpolung). die niedrigere Qualität ist jedoch häufig nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="3e289-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="3e289-143">Im nächsten Abschnitt erfahren Sie, wie Sie mit Direct3D 10 die Block Komprimierung in Ihrer Anwendung ganz einfach verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3e289-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="3e289-144">Verwenden von Block Komprimierung</span><span class="sxs-lookup"><span data-stu-id="3e289-144">Using Block Compression</span></span>

<span data-ttu-id="3e289-145">Erstellen Sie eine Block komprimierte Textur wie eine nicht komprimierte Textur (siehe [Create a texture from a file](d3d10-graphics-programming-guide-resources-creating-textures.md)), mit dem Unterschied, dass Sie ein Block komprimiertes Format angeben.</span><span class="sxs-lookup"><span data-stu-id="3e289-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="3e289-146">Erstellen Sie als nächstes eine Ansicht, um die Textur an die Pipeline zu binden.</span><span class="sxs-lookup"><span data-stu-id="3e289-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="3e289-147">Da eine Block komprimierte Textur nur als Eingabe für eine Shader-Phase verwendet werden kann, sollten Sie eine Shader-Ressourcen Ansicht erstellen, indem Sie [**createshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3e289-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="3e289-148">Verwenden Sie eine komprimierte-Struktur auf die gleiche Weise wie eine nicht komprimierte Textur.</span><span class="sxs-lookup"><span data-stu-id="3e289-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="3e289-149">Wenn Ihre Anwendung einen Speicher Zeiger auf Block komprimierte Daten erhält, müssen Sie die Speicher Auffüll Zeichen in einer MipMap berücksichtigen, die bewirkt, dass die deklarierte Größe von der tatsächlichen Größe abweicht.</span><span class="sxs-lookup"><span data-stu-id="3e289-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="3e289-150">Virtuelle Größe im Vergleich zur physischen Größe</span><span class="sxs-lookup"><span data-stu-id="3e289-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="3e289-151">Wenn Sie über Anwendungscode verfügen, in dem ein Speicher Zeiger zum Durchlaufen des Speichers einer komprimierten Blocktextur verwendet wird, ist ein wichtiger Aspekt zu beachten, der möglicherweise eine Änderung des Anwendungs Codes erfordert.</span><span class="sxs-lookup"><span data-stu-id="3e289-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="3e289-152">Eine Block komprimierte Textur muss ein Vielfaches von 4 in allen Dimensionen sein, da die Block Komprimierungs Algorithmen auf 4 x 4 texverblöcken angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="3e289-153">Dies stellt ein Problem für eine MipMap dar, deren anfängliche Dimensionen durch 4 teilbar sind, die unterteilten Ebenen jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="3e289-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="3e289-154">Das folgende Diagramm zeigt den Unterschied zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe der einzelnen MipMap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="3e289-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![Diagramm der nicht komprimierten und komprimierten MipMap-Ebenen](images/d3d10-block-compress-pad.png)

<span data-ttu-id="3e289-156">Die linke Seite des Diagramms zeigt die Größen der MipMap-Ebenen an, die für eine unkomprimierte 60 × 40-Textur generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="3e289-157">Der API-Befehl, der die Textur generiert, wird auf oberster Ebene festgenommen. jede nachfolgende Ebene ist die Hälfte der Größe der vorherigen Ebene.</span><span class="sxs-lookup"><span data-stu-id="3e289-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="3e289-158">Bei einer nicht komprimierten Textur besteht kein Unterschied zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe.</span><span class="sxs-lookup"><span data-stu-id="3e289-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="3e289-159">Auf der rechten Seite des Diagramms werden die Größen der MipMap-Ebene angezeigt, die für die gleiche 60 × 40-Textur mit Komprimierung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="3e289-160">Beachten Sie, dass die zweite und die dritte Ebene eine Speicher Auffüll Zeichen aufweisen, um die Größen Faktoren 4 auf jeder Ebene zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3e289-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="3e289-161">Dies ist erforderlich, damit die Algorithmen in 4 × 4 textexblöcken betrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="3e289-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="3e289-162">Dies ist besonders offensichtlich, wenn MipMap-Ebenen in Erwägung gezogen werden, die kleiner sind als 4 × 4. die Größe dieser sehr kleinen MipMap-Ebenen wird auf den nächstgelegenen Faktor 4 aufgerundet, wenn Texturspeicher zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="3e289-163">Sampling der Hardware verwendet die virtuelle Größe. Beim Sampling der Textur wird die Arbeitsspeicher Auffüll Zeichen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3e289-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="3e289-164">Bei MipMap-Ebenen, die kleiner als 4 × 4 sind, werden nur die ersten vier texeln für eine 2 × 2-Karte verwendet, und nur die ersten texeln werden von einem 1 × 1-Block verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e289-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="3e289-165">Es gibt jedoch keine API-Struktur, die die physische Größe (einschließlich des Speicher Paddings) verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3e289-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="3e289-166">Beachten Sie bei der Zusammenfassung die Verwendung von ausgerichteten Speicherblöcken beim Kopieren von Regionen, die Block komprimierte Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e289-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="3e289-167">Um dies in einer Anwendung zu erreichen, die einen Speicher Zeiger abruft, stellen Sie sicher, dass der Zeiger die Oberflächendarstellung verwendet, um die Größe des physischen Speichers zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3e289-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="3e289-168">Komprimierungs Algorithmen</span><span class="sxs-lookup"><span data-stu-id="3e289-168">Compression Algorithms</span></span>

<span data-ttu-id="3e289-169">Die Verfahren zur Block Komprimierung in Direct3D unterbrechen unkomprimierte Textur Daten in 4 × 4-Blöcke, komprimieren jeden Block und speichern die Daten.</span><span class="sxs-lookup"><span data-stu-id="3e289-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="3e289-170">Daher wird erwartet, dass Texturen komprimierte Textur Dimensionen aufweisen, die vielfachen von 4 sind.</span><span class="sxs-lookup"><span data-stu-id="3e289-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![Diagramm der Block Komprimierung](images/d3d10-compression-1.png)

<span data-ttu-id="3e289-172">Das vorangehende Diagramm zeigt eine Textur, die in texblöcke partitioniert ist.</span><span class="sxs-lookup"><span data-stu-id="3e289-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="3e289-173">Der erste Block zeigt das Layout der 16 texeln mit der Bezeichnung a-p an, aber jeder Block verfügt über dieselbe Organisation der Daten.</span><span class="sxs-lookup"><span data-stu-id="3e289-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="3e289-174">Direct3D implementiert mehrere Komprimierungs Schemas, von denen jedes einen anderen Kompromiss zwischen der Anzahl gespeicherter Komponenten, der Anzahl der Bits pro Komponente und dem verbrauchten Arbeitsspeicher implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e289-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="3e289-175">Verwenden Sie diese Tabelle, um das Format auszuwählen, das am besten mit dem Datentyp und der Datenauflösung funktioniert, die für Ihre Anwendung am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3e289-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="3e289-176">Quelldaten</span><span class="sxs-lookup"><span data-stu-id="3e289-176">Source Data</span></span>                     | <span data-ttu-id="3e289-177">Auflösung der Datenkomprimierung (in Bits)</span><span class="sxs-lookup"><span data-stu-id="3e289-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="3e289-178">Dieses Komprimierungs Format auswählen</span><span class="sxs-lookup"><span data-stu-id="3e289-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="3e289-179">Farbe und Alpha der drei Komponenten</span><span class="sxs-lookup"><span data-stu-id="3e289-179">Three-component color and alpha</span></span> | <span data-ttu-id="3e289-180">Farbe (5:6:5), Alpha (1) oder kein Alpha</span><span class="sxs-lookup"><span data-stu-id="3e289-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="3e289-181">BC1</span><span class="sxs-lookup"><span data-stu-id="3e289-181">BC1</span></span>                            |
| <span data-ttu-id="3e289-182">Farbe und Alpha der drei Komponenten</span><span class="sxs-lookup"><span data-stu-id="3e289-182">Three-component color and alpha</span></span> | <span data-ttu-id="3e289-183">Farbe (5:6:5), Alpha (4)</span><span class="sxs-lookup"><span data-stu-id="3e289-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="3e289-184">BU2</span><span class="sxs-lookup"><span data-stu-id="3e289-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="3e289-185">Farbe und Alpha der drei Komponenten</span><span class="sxs-lookup"><span data-stu-id="3e289-185">Three-component color and alpha</span></span> | <span data-ttu-id="3e289-186">Farbe (5:6:5), Alpha (8)</span><span class="sxs-lookup"><span data-stu-id="3e289-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="3e289-187">BC3</span><span class="sxs-lookup"><span data-stu-id="3e289-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="3e289-188">Farbe mit einer Komponente</span><span class="sxs-lookup"><span data-stu-id="3e289-188">One-component color</span></span>             | <span data-ttu-id="3e289-189">Eine Komponente (8)</span><span class="sxs-lookup"><span data-stu-id="3e289-189">One component (8)</span></span>                     | [<span data-ttu-id="3e289-190">BC4</span><span class="sxs-lookup"><span data-stu-id="3e289-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="3e289-191">Farbe mit zwei Komponenten</span><span class="sxs-lookup"><span data-stu-id="3e289-191">Two-component color</span></span>             | <span data-ttu-id="3e289-192">Zwei Komponenten (8:8)</span><span class="sxs-lookup"><span data-stu-id="3e289-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="3e289-193">BC5</span><span class="sxs-lookup"><span data-stu-id="3e289-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="3e289-194">BC1</span><span class="sxs-lookup"><span data-stu-id="3e289-194">BC1</span></span>

<span data-ttu-id="3e289-195">Verwenden Sie das erste Block Komprimierungs Format (BC1) (entweder DXGI- \_ Format \_ BC1 \_ typlose, DXGI- \_ Format \_ BC1 \_ unorm oder DXGI \_ BC1 \_ unorm \_ sRGB), um mithilfe einer 5:6:5-Farbe (5 Bits rot, 6 Bits grün, 5 Bits blau) Daten mit drei Komponenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3e289-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="3e289-196">Dies gilt auch, wenn die Daten auch 1-Bit-Alpha enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e289-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="3e289-197">Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat verwendet wird, verringert das BC1-Format den benötigten Arbeitsspeicher von 48 Byte (16 Farben × 3 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Bytes Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e289-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="3e289-198">Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="3e289-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="3e289-199">Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Verweis Farben (Farbe \_ 0 und Farbe \_ 1) und 16 2-Bit-Farbindizes (blockiert ein – p), wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![Diagramm des Layouts für die BC1-Komprimierung](images/d3d10-compression-bc1.png)

<span data-ttu-id="3e289-201">Die Farbindizes (a – p) werden verwendet, um die ursprünglichen Farben aus einer Farbtabelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3e289-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="3e289-202">Die Farbtabelle enthält 4 Farben.</span><span class="sxs-lookup"><span data-stu-id="3e289-202">The color table contains 4 colors.</span></span> <span data-ttu-id="3e289-203">Die ersten beiden Farben – Color \_ 0 und Color \_ 1 – sind die Mindest-und höchst Farben.</span><span class="sxs-lookup"><span data-stu-id="3e289-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="3e289-204">Bei den anderen beiden Farben (Farbe \_ 2 und Farbe \_ 3) handelt es sich um zwischen Farben, die mit linearer Interpolationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="3e289-205">Die vier Farben sind 2-Bit-Indexwerte zugewiesen, die in Blocks a – p gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="3e289-206">Schließlich wird jede der Farben in Blocks a – p mit den vier Farben in der Farbtabelle verglichen, und der Index für die nächstgelegene Farbe wird in den 2-Bit-Blöcken gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3e289-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="3e289-207">Dieser Algorithmus eignet sich für Daten, die auch 1-Bit-Alpha enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e289-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="3e289-208">Der einzige Unterschied besteht darin, dass Farbe \_ 3 auf 0 festgelegt ist (was eine transparente Farbe darstellt) und Farbe \_ 2 eine lineare Mischung aus Farbe \_ 0 und Farbe \_ 1 ist.</span><span class="sxs-lookup"><span data-stu-id="3e289-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e289-209">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3e289-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="3e289-210">Dieses Format ist sowohl in Direct3D 9 als auch in 10 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3e289-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="3e289-211">In Direct3D 9 wird das BC1-Format als D3DFMT_DXT1 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e289-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="3e289-212">In Direct3D 10 wird das BC1-Format durch DXGI_FORMAT_BC1_UNORM oder DXGI_FORMAT_BC1_UNORM_SRGB dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="3e289-213">BU2</span><span class="sxs-lookup"><span data-stu-id="3e289-213">BC2</span></span>

<span data-ttu-id="3e289-214">Verwenden Sie das BC2-Format (entweder DXGI- \_ Format \_ BC2 \_ typlose, DXGI- \_ Format \_ BC2 \_ unorm oder DXGI \_ BC2 \_ unorm \_ sRGB), um Daten zu speichern, die Farb-und Alpha Daten mit geringer Kohärenz enthalten (verwenden Sie [BC3](#bc3) für hochgradig kohärente Alpha-Daten).</span><span class="sxs-lookup"><span data-stu-id="3e289-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="3e289-215">Das BC2-Format speichert RGB-Daten als 5:6:5-Farbe (5 Bits rot, 6 Bits grün, 5 Bits blau) und Alpha als separaten 4-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="3e289-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="3e289-216">Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert dieses Komprimierungs Verfahren den von 64 bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes an Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e289-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="3e289-217">Das Format BC2 speichert Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1](#bc1) -Format. für BC2 sind jedoch zusätzliche 64-Bits Arbeitsspeicher erforderlich, um die Alpha Daten zu speichern, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![Diagramm des Layouts für die BC2-Komprimierung](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e289-219">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3e289-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="3e289-220">Dieses Format ist sowohl in Direct3D 9 als auch in 10 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3e289-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="3e289-221">In Direct3D 9 wird das BC2-Format als D3DFMT_DXT2 und D3DFMT_DXT3 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e289-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="3e289-222">In Direct3D 10 wird das BC2-Format durch DXGI_FORMAT_BC2_UNORM oder DXGI_FORMAT_BC2_UNORM_SRGB dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="3e289-223">BC3</span><span class="sxs-lookup"><span data-stu-id="3e289-223">BC3</span></span>

<span data-ttu-id="3e289-224">Verwenden Sie das BC3-Format (entweder DXGI- \_ Format \_ BC3 \_ typlose, DXGI- \_ Format \_ BC3 \_ unorm oder DXGI \_ BC3 \_ unorm \_ sRGB), um hochgradig kohärente Farbdaten zu speichern (verwenden Sie [BC2](#bc2) mit weniger kohärenten Alpha Daten).</span><span class="sxs-lookup"><span data-stu-id="3e289-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="3e289-225">Das Format BC3 speichert Farbdaten mit einer Farbe von 5:6:5 (5 Bits rot, 6 Bits grün, 5 Bits blau) und Alpha Daten mithilfe eines Bytes.</span><span class="sxs-lookup"><span data-stu-id="3e289-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="3e289-226">Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert dieses Komprimierungs Verfahren den von 64 bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes an Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e289-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="3e289-227">Das Format BC3 speichert Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1](#bc1) -Format. für BC3 sind jedoch zusätzliche 64-Bits Arbeitsspeicher erforderlich, um die Alpha Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3e289-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="3e289-228">Das BC3-Format verarbeitet Alpha durch die Speicherung zweier Verweis Werte und interpolieren zwischen Ihnen (ähnlich wie BC1 die RGB-Farbe speichert).</span><span class="sxs-lookup"><span data-stu-id="3e289-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="3e289-229">Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="3e289-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="3e289-230">Anstatt 16 Alpha-Werte zu speichern, speichert der Algorithmus 2 Reference Premultiplied (Alpha \_ 0 und Alpha \_ 1) und 16 3-Bit-Farbindizes (Alpha a bis p), wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![Diagramm des Layouts für die BC3-Komprimierung](images/d3d10-compression-bc3.png)

<span data-ttu-id="3e289-232">Das BC3-Format verwendet die Alpha Indizes (a – p), um die ursprünglichen Farben aus einer Nachschlage Tabelle zu suchen, die 8 Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="3e289-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="3e289-233">Die ersten beiden Werte – Alpha \_ 0 und Alpha \_ 1 – sind die Mindest-und Höchstwerte. die anderen sechs Zwischenwerte werden mithilfe von linearer Interpolationen berechnet.</span><span class="sxs-lookup"><span data-stu-id="3e289-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="3e289-234">Der Algorithmus bestimmt die Anzahl der interpoliert Alpha Werte durch Untersuchen der beiden Referenz-Alpha-Werte.</span><span class="sxs-lookup"><span data-stu-id="3e289-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="3e289-235">Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, interpoliert BC3 6 alpha Werte, andernfalls wird 4 interpoliert.</span><span class="sxs-lookup"><span data-stu-id="3e289-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="3e289-236">Wenn BC3 nur 4 alpha-Werte interpoliert, werden zwei zusätzliche Alpha Werte festgelegt (0 für vollständig transparent und 255 für vollständig deckend).</span><span class="sxs-lookup"><span data-stu-id="3e289-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="3e289-237">BC3 komprimiert die Alpha Werte im 4 × 4-texesbereich, indem der Bitcode gespeichert wird, der den interinterpolierten Alpha Werten entspricht, die am ehesten mit dem ursprünglichen Alpha für ein bestimmtes Texel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3e289-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e289-238">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3e289-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="3e289-239">In Direct3D 9 wird das BC3-Format als D3DFMT_DXT4 und D3DFMT_DXT5 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e289-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="3e289-240">In Direct3D 10 wird das BC3-Format durch DXGI_FORMAT_BC3_UNORM oder DXGI_FORMAT_BC3_UNORM_SRGB dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="3e289-241">BC4</span><span class="sxs-lookup"><span data-stu-id="3e289-241">BC4</span></span>

<span data-ttu-id="3e289-242">Verwenden Sie das BC4-Format, um Farbdaten mit einer Komponente in 8 Bits für jede Farbe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3e289-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="3e289-243">Aufgrund der zunehmenden Genauigkeit (im Vergleich zu [BC1](#bc1)) ist BC4 ideal für das Speichern von Gleit Komma Daten im Bereich von \[ 0 bis 1 \] . dabei wird das DXGI \_ -Format \_ BC4 \_ unorm-Format und \[ -1 bis + 1 \] verwendet, wobei das DXGI- \_ Format \_ BC4 \_ snorm-Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="3e289-244">Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert diese Komprimierungs Technik den benötigten Arbeitsspeicher von 16 Bytes (16 Farben × 1 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Bytes.</span><span class="sxs-lookup"><span data-stu-id="3e289-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="3e289-245">Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="3e289-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="3e289-246">Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Verweis Farben (rot \_ 0 und rot \_ 1) und 16 3-Bit-Farbindizes (rot a bis rot p), wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![Diagramm des Layouts für die BC4-Komprimierung](images/d3d10-compression-bc4.png)

<span data-ttu-id="3e289-248">Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle zu suchen, die 8 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="3e289-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="3e289-249">Die ersten beiden Farben – rot \_ 0 und rot \_ 1 – sind die Mindest-und höchst Farben.</span><span class="sxs-lookup"><span data-stu-id="3e289-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="3e289-250">Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen interpolung.</span><span class="sxs-lookup"><span data-stu-id="3e289-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="3e289-251">Der Algorithmus bestimmt die Anzahl der interpoliert Farbwerte durch Untersuchen der beiden Referenzwerte.</span><span class="sxs-lookup"><span data-stu-id="3e289-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="3e289-252">Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC4 sechs Farbwerte, andernfalls wird 4 interpoliert.</span><span class="sxs-lookup"><span data-stu-id="3e289-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="3e289-253">Wenn BC4 nur 4 Farbwerte interpoliert, werden zwei zusätzliche Farbwerte festgelegt (0,0 f für vollständig transparent und 1.0 f für vollständig nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="3e289-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="3e289-254">BC4 komprimiert die Alpha Werte im 4 × 4-texesbereich, indem der Bitcode gespeichert wird, der den interpoliert Alpha-Werten entspricht, die am ehesten mit dem ursprünglichen Alpha für eine bestimmte textexelle übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3e289-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="3e289-255">BC4 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="3e289-256">BC4 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="3e289-257">BC4 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-257">BC4\_UNORM</span></span>

<span data-ttu-id="3e289-258">Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="3e289-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="3e289-259">Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="3e289-260">BC4 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-260">BC4\_SNORM</span></span>

<span data-ttu-id="3e289-261">Das DXGI- \_ Format \_ BC4 \_ snorm ist exakt identisch, mit der Ausnahme, dass die Daten im snorm-Bereich codiert werden und wenn 4 Farbwerte interpoliert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="3e289-262">Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="3e289-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="3e289-263">Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="3e289-264">BC5</span><span class="sxs-lookup"><span data-stu-id="3e289-264">BC5</span></span>

<span data-ttu-id="3e289-265">Verwenden Sie das BC5-Format, um Farbdaten mit zwei Komponenten zu speichern, wobei für jede Farbe 8 Bits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="3e289-266">Aufgrund der zunehmenden Genauigkeit (im Vergleich zu [BC1](#bc1)) ist BC5 ideal für das Speichern von Gleit Komma Daten im Bereich von \[ 0 bis 1 \] . dabei wird das DXGI \_ -Format \_ BC5 \_ unorm-Format und \[ -1 bis + 1 \] verwendet, wobei das DXGI- \_ Format \_ BC5 \_ snorm-Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e289-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="3e289-267">Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert diese Komprimierungs Technik den von 32 Bytes (16 Farben × 2 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes.</span><span class="sxs-lookup"><span data-stu-id="3e289-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="3e289-268">Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="3e289-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="3e289-269">Anstatt für beide Komponenten 16 Farben zu speichern, speichert der Algorithmus zwei Verweis Farben für jede Komponente (rot \_ 0, rot \_ 1, grün \_ 0 und grün \_ 1) und 16 3-Bit-Farbindizes für jede Komponente (rot a bis rot und grün a durch grünes p), wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e289-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![Diagramm des Layouts für die BC5-Komprimierung](images/d3d10-compression-bc5.png)

<span data-ttu-id="3e289-271">Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle zu suchen, die 8 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="3e289-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="3e289-272">Die ersten beiden Farben – rot \_ 0 und rot \_ 1 (oder grün \_ und grün \_ 1) – sind die Mindest-und höchst Farben.</span><span class="sxs-lookup"><span data-stu-id="3e289-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="3e289-273">Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen interpolung.</span><span class="sxs-lookup"><span data-stu-id="3e289-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="3e289-274">Der Algorithmus bestimmt die Anzahl der interpoliert Farbwerte durch Untersuchen der beiden Referenzwerte.</span><span class="sxs-lookup"><span data-stu-id="3e289-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="3e289-275">Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC5 sechs Farbwerte, andernfalls wird 4 interpoliert.</span><span class="sxs-lookup"><span data-stu-id="3e289-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="3e289-276">Wenn BC5 nur 4 Farbwerte interpoliert, werden die verbleibenden beiden Farbwerte bei 0,0 f und 1.0 f festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e289-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="3e289-277">BC5 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="3e289-278">BC5 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="3e289-279">BC5 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-279">BC5\_UNORM</span></span>

<span data-ttu-id="3e289-280">Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="3e289-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="3e289-281">Die Berechnungen für die grünen Komponenten sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="3e289-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="3e289-282">Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="3e289-283">BC5 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-283">BC5\_SNORM</span></span>

<span data-ttu-id="3e289-284">Das DXGI- \_ Format \_ BC5 \_ snorm ist exakt identisch, mit der Ausnahme, dass die Daten im snorm-Bereich codiert werden und wenn 4 Datenwerte interpoliert werden, sind die beiden zusätzlichen Werte-1.0 f und 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="3e289-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="3e289-285">Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="3e289-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="3e289-286">Die Berechnungen für die grünen Komponenten sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="3e289-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="3e289-287">Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="3e289-288">Format Konvertierung mit Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="3e289-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="3e289-289">Direct3D 10,1 ermöglicht Kopien zwischen vorstrukturierten typisierten Texturen und Block komprimierten Texturen derselben Bitbreite.</span><span class="sxs-lookup"><span data-stu-id="3e289-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="3e289-290">Die Funktionen, die dies erreichen können, sind [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="3e289-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="3e289-291">Ab Direct3D 10,1 können Sie [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) zum Kopieren zwischen einigen Format Typen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e289-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="3e289-292">Diese Art von Kopiervorgang führt einen Typ von Formatkonvertierung aus, bei dem Ressourcen Daten in einem anderen Formattyp neu interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e289-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="3e289-293">Sehen Sie sich dieses Beispiel an, in dem der Unterschied zwischen dem erneuten interpretieren von Daten mit der Art und Weise dargestellt wird, in der sich die</span><span class="sxs-lookup"><span data-stu-id="3e289-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="3e289-294">Verwenden Sie [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy), um "f" als Typ von "u" neu zu interpretieren:</span><span class="sxs-lookup"><span data-stu-id="3e289-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="3e289-295">In der obigen Neuinterpretation ändert sich der zugrunde liegende Wert der Daten nicht. [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) interpretiert den float-Wert als ganze Zahl ohne Vorzeichen neu.</span><span class="sxs-lookup"><span data-stu-id="3e289-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="3e289-296">Verwenden Sie zum Ausführen der typischen Art der Konvertierung die Zuweisung:</span><span class="sxs-lookup"><span data-stu-id="3e289-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="3e289-297">In der vorangehenden Konvertierung ändert sich der zugrunde liegende Wert der Daten.</span><span class="sxs-lookup"><span data-stu-id="3e289-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="3e289-298">In der folgenden Tabelle werden die zulässigen Quell-und Zielformate aufgelistet, die Sie in diesem neuinterpretertyp der Formatkonvertierung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3e289-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="3e289-299">Sie müssen die Werte ordnungsgemäß codieren, damit die Neuinterpretation erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3e289-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="3e289-300">Bitbreite</span><span class="sxs-lookup"><span data-stu-id="3e289-300">Bit Width</span></span> | <span data-ttu-id="3e289-301">Nicht komprimierte Ressource</span><span class="sxs-lookup"><span data-stu-id="3e289-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="3e289-302">Block-Compressed-Ressource</span><span class="sxs-lookup"><span data-stu-id="3e289-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e289-303">32</span><span class="sxs-lookup"><span data-stu-id="3e289-303">32</span></span>        | <span data-ttu-id="3e289-304">DXGI- \_ Format \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3e289-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="3e289-305">DXGI- \_ Format \_ R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3e289-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="3e289-306">DXGI- \_ Format \_ R9G9B9E5 \_ sharedexp</span><span class="sxs-lookup"><span data-stu-id="3e289-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="3e289-307">64</span><span class="sxs-lookup"><span data-stu-id="3e289-307">64</span></span>        | <span data-ttu-id="3e289-308">DXGI- \_ Format \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3e289-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="3e289-309">DXGI- \_ Format \_ R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3e289-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="3e289-310">DXGI- \_ Format \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3e289-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="3e289-311">DXGI- \_ Format \_ R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3e289-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="3e289-312">DXGI- \_ Format \_ BC1 \_ unorm \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="3e289-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="3e289-313">DXGI- \_ Format \_ BC4 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="3e289-314">DXGI- \_ Format \_ BC4 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="3e289-315">128</span><span class="sxs-lookup"><span data-stu-id="3e289-315">128</span></span>       | <span data-ttu-id="3e289-316">DXGI- \_ Format \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3e289-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="3e289-317">DXGI- \_ Format \_ R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3e289-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="3e289-318">DXGI- \_ Format \_ BC2 \_ unorm \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="3e289-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="3e289-319">DXGI- \_ Format \_ BC3 \_ unorm \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="3e289-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="3e289-320">DXGI- \_ Format \_ BC5 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="3e289-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="3e289-321">DXGI- \_ Format \_ BC5 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="3e289-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3e289-322">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e289-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e289-323">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3e289-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
