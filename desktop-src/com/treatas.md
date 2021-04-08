---
title: Behandlungen
description: Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Registrierungsschlüssel für TreatAs com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856399"
---
# <a name="treatas"></a><span data-ttu-id="67741-104">Behandlungen</span><span class="sxs-lookup"><span data-stu-id="67741-104">TreatAs</span></span>

<span data-ttu-id="67741-105">Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.</span><span class="sxs-lookup"><span data-stu-id="67741-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="67741-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="67741-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="67741-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67741-107">Remarks</span></span>

<span data-ttu-id="67741-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="67741-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="67741-109">Emulation ist die Fähigkeit einer Anwendung, ein Objekt einer anderen Klasse zu öffnen und zu bearbeiten, wobei das ursprüngliche Format des Objekts beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="67741-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="67741-110">Die Lösung erfolgt auf dem lokalen Computer, sodass bei der Remote Aktivierung die Auflösung auf dem Client Computer unter Verwendung der von **TreatAs** angegebenen CLSID erfolgt.</span><span class="sxs-lookup"><span data-stu-id="67741-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="67741-111">DCOM prüft die lokale Registrierung für **TreatAs**, auch wenn Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen und einen Remote Server angeben.</span><span class="sxs-lookup"><span data-stu-id="67741-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="67741-112">Dies bedeutet Folgendes: Wenn Sie einen **behandateneintrag** für Class1 haben, der auf dem lokalen Computer als Klasse2 behandelt werden soll, wenn Sie jedoch **cokreateinstance** aufrufen, um eine Instanz von Class1 zu erstellen und einen Remote Server anzugeben, versucht DCOM, eine Instanz von Klasse2 auf dem Remote Server zu erstellen, auch wenn Klasse2 nicht auf dem Remote Server registriert ist, was dazu führt, dass der **cokreateinstance** -Befehl fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="67741-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67741-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67741-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67741-114">**AutoTreatAs**</span><span class="sxs-lookup"><span data-stu-id="67741-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="67741-115">**Cogettreatasclass**</span><span class="sxs-lookup"><span data-stu-id="67741-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="67741-116">**Cotreatasclass**</span><span class="sxs-lookup"><span data-stu-id="67741-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




