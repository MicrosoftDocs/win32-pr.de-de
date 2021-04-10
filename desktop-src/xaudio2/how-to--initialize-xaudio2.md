---
description: XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine erstellt und eine Mastering-Stimme erstellt wird.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: "So wird's gemacht: Initialisieren von XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862951"
---
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="da198-103">So wird's gemacht: Initialisieren von XAudio2</span><span class="sxs-lookup"><span data-stu-id="da198-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="da198-104">XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine erstellt und eine Mastering-Stimme erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="da198-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="da198-105">**So initialisieren Sie XAudio2**</span><span class="sxs-lookup"><span data-stu-id="da198-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="da198-106">Stellen Sie sicher, dass Sie com initialisiert haben.</span><span class="sxs-lookup"><span data-stu-id="da198-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="da198-107">Für eine Windows Store-App erfolgt dies im Rahmen der Initialisierung der Windows-Runtime.</span><span class="sxs-lookup"><span data-stu-id="da198-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="da198-108">Andernfalls verwenden Sie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="da198-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="da198-109">Verwenden Sie die [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) -Funktion, um eine Instanz der XAudio2-Engine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da198-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="da198-110">Verwenden Sie die Methode " [**kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) ", um eine Stimme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da198-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="da198-111">Die Mastering-Stimmen Kapseln ein Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="da198-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="da198-112">Es ist das ultimative Ziel für alle Audiodaten, die über ein audiodiagramm geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="da198-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="da198-113">Hinweise für Windows Store-Apps</span><span class="sxs-lookup"><span data-stu-id="da198-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="da198-114">Es wird empfohlen, einen [intelligenten Zeiger](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf sichere Weise zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="da198-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="da198-115">Für Windows Store-Apps können Sie die Vorlage " [**comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) -intelligenter Zeiger" aus der Windows-Runtime C++ Template Library (WRL) verwenden.</span><span class="sxs-lookup"><span data-stu-id="da198-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> <span data-ttu-id="da198-116">Stellen Sie sicher, dass alle untergeordneten XAUDIO2-Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Objekt</span><span class="sxs-lookup"><span data-stu-id="da198-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da198-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da198-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da198-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="da198-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="da198-119">So wird's gemacht: Laden von Datendateien in XAudio2</span><span class="sxs-lookup"><span data-stu-id="da198-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="da198-120">So wird's gemacht: Wiedergeben von Ton mit XAudio2</span><span class="sxs-lookup"><span data-stu-id="da198-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
