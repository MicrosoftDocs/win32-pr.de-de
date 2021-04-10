---
title: Erstellen eines Riff Segments
description: Erstellen eines Riff Segments
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- Multimedia-Datei-e/a, Erstellen von Riff Segmenten
- Datei-e/a, Erstellen eines Riff Segments
- Eingabe und Ausgabe (e/a), Erstellen eines Riff Blocks
- E/a (Eingabe und Ausgabe), Erstellen eines Riff Blocks
- Erstellen eines Riff Segments
- mmiokreatechunk-Funktion
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858205"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="89368-113">Erstellen eines Riff Segments</span><span class="sxs-lookup"><span data-stu-id="89368-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="89368-114">Im folgenden Beispiel wird die [**mmiokreatechunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) -Funktion verwendet, um einen Block mit dem Block Bezeichner "Riff" und dem Formulartyp "rdib" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89368-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="89368-115">Wenn Sie einen "Riff"-oder "List"-Block erstellen, müssen Sie den Formulartyp oder den Listentyp im **fcctype** -Member der [**mmckinfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="89368-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="89368-116">Im vorherigen Beispiel ist "rdib" der Formulartyp.</span><span class="sxs-lookup"><span data-stu-id="89368-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="89368-117">Wenn Sie die Größe des Daten Felds in einem neuen Block kennen, können Sie den **cksize** -Member der **mmckinfo** -Struktur festlegen, wenn Sie den Block erstellen.</span><span class="sxs-lookup"><span data-stu-id="89368-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="89368-118">Dieser Wert wird in das Feld Datengröße im neuen Block geschrieben.</span><span class="sxs-lookup"><span data-stu-id="89368-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="89368-119">Wenn dieser Wert nicht korrekt ist, wenn Sie [**mmioascend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) zum Markieren des Blocks enden, wird er automatisch umgeschrieben, um die korrekte Größe des Daten Felds widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="89368-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="89368-120">Nachdem Sie mithilfe der [**mmiokreatechunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) -Funktion einen Block erstellt haben, wird die Dateiposition auf das Datenfeld des Blocks (8 Bytes vom Anfang des Blocks) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89368-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="89368-121">Wenn es sich bei dem Block um einen "Riff"-oder "List"-Block handelt, wird die Dateiposition auf den Speicherort festgelegt, der dem Typ oder dem Auflistungstyp folgt (12 Bytes vom Anfang des Blocks).</span><span class="sxs-lookup"><span data-stu-id="89368-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 