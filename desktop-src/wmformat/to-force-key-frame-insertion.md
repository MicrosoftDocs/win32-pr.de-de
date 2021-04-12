---
title: So erzwingen Sie Key-Frame einfügen
description: So erzwingen Sie Key-Frame einfügen
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), Erzwingen von Tasten Frame-Einfügungen
- ASF (Advanced Systems Format), Erzwingen von Tasten Frame-Einfügungen
- Advanced Systems Format (ASF), Keyframe-Einfügungen
- ASF (Advanced Systems Format), Keyframe-Einfügungen
- Keyframes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472389"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="1cf03-108">So erzwingen Sie Key-Frame einfügen</span><span class="sxs-lookup"><span data-stu-id="1cf03-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="1cf03-109">Der Windows Media Video 9-Codec unterstützt erzwungene Keyframe-Einfügevorgänge.</span><span class="sxs-lookup"><span data-stu-id="1cf03-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="1cf03-110">Wenn Sie ein Beispiel an den Writer übergeben, können Sie angeben, dass es als [*Keyframe*](wmformat-glossary.md)codiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1cf03-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="1cf03-111">Führen Sie die folgenden Schritte aus, um das Einfügen von Schlüsseln für ein Beispiel zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="1cf03-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="1cf03-112">Weisen Sie einen Puffer zum Speichern des Beispiels zu, und rufen Sie einen Zeiger auf die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle ab, die den Puffer durch Aufrufen von [**iwmwriter:: allopriesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf03-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="1cf03-113">Rufen Sie den Speicherort und die Größe des Puffers ab, der in Schritt 1 erstellt wurde, indem Sie [**inssbuffer:: getbufferandlength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1cf03-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="1cf03-114">Kopieren Sie die Beispiel Daten in den Puffer Speicherort, und stellen Sie sicher, dass das Beispiel erfolgreich in den zugeordneten Puffer passt.</span><span class="sxs-lookup"><span data-stu-id="1cf03-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="1cf03-115">Abhängig von der Quelle der Beispiele können Sie eine Vielzahl von Funktionen verwenden, um die Daten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1cf03-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="1cf03-116">Wenn Sie z. b. einen Stream aus einer AVI-Datei kopieren, können Sie die AVI-Funktion **avistreamread** verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cf03-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="1cf03-117">Aktualisieren Sie die im Puffer verwendete Datenmenge, um die tatsächliche Größe des Beispiels durch Aufrufen von " [**inssbuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)" widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="1cf03-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="1cf03-118">Abrufen eines Zeigers auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle durch Aufrufen von " **inssbuffer:: QueryInterface**".</span><span class="sxs-lookup"><span data-stu-id="1cf03-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="1cf03-119">Legen Sie das Beispiel als erzwungener Keyframe fest, indem Sie die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode aufrufen, um die "WM \_ sampleextensionguid \_ outputcleanpoint"-Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1cf03-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="1cf03-120">Diese Eigenschaft ist ein boolescher Wert. Legen Sie diese Einstellung auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="1cf03-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="1cf03-121">Übergeben Sie die Puffer Schnittstelle zusammen mit der Eingabe Nummer und der Beispiel Zeit mithilfe der Methode [**iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) an den Writer.</span><span class="sxs-lookup"><span data-stu-id="1cf03-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cf03-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1cf03-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cf03-123">**Iwmwriter:: schreitesample**</span><span class="sxs-lookup"><span data-stu-id="1cf03-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="1cf03-124">**So schreiben Sie Beispiele**</span><span class="sxs-lookup"><span data-stu-id="1cf03-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="1cf03-125">**Codierung der Variablen Bitrate (VBR)**</span><span class="sxs-lookup"><span data-stu-id="1cf03-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="1cf03-126">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="1cf03-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




