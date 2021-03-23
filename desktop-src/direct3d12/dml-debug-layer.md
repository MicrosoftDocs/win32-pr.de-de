---
title: Verwenden der directml-debugschicht
description: Die directml-debugschicht ist eine optionale Entwicklungszeit Komponente, die Sie beim Debuggen Ihres directml-Codes unterstützt.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548685"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="bc228-103">Verwenden der directml-debugschicht</span><span class="sxs-lookup"><span data-stu-id="bc228-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="bc228-104">Die directml-debugschicht ist eine optionale Entwicklungszeit Komponente, die Sie beim Debuggen Ihres directml-Codes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc228-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="bc228-105">Die Debug-Ebene ist Teil eines separaten Grafik Toolpakets, das als [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD) verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="bc228-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="bc228-106">Die Grafik Tools-FOD muss auf dem System installiert sein, damit die Debugebene verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc228-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="bc228-107">Es wird dringend empfohlen, dass Sie die debugschicht bei der Entwicklung von Anwendungen mithilfe von directml aktivieren, da Sie im Falle einer ungültigen API-Verwendung wertvolle Informationen bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="bc228-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="bc228-108">Installieren der directml-debugschicht</span><span class="sxs-lookup"><span data-stu-id="bc228-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="bc228-109">Um das optionale FOD-Paket (Feature-on-Demand) für Grafik Tools zu installieren, führen Sie den folgenden Befehl an einer PowerShell-Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="bc228-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="bc228-110">Alternativ können Sie das Grafik Toolpaket in den Windows 10-Einstellungen installieren.</span><span class="sxs-lookup"><span data-stu-id="bc228-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="bc228-111">Navigieren Sie zu **Einstellungen**  >  **apps** apps  >  **& Features**  >  **optionale Features Features**  >  **Hinzufügen** > und wählen Sie dann **Grafik Tools** aus.</span><span class="sxs-lookup"><span data-stu-id="bc228-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="bc228-112">Aktivieren der directml-debugschicht</span><span class="sxs-lookup"><span data-stu-id="bc228-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="bc228-113">Sobald das Grafik Tools-Paket installiert ist, können Sie die directml-debugschicht durch Bereitstellen von  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) aktivieren, wenn Sie [**dmlkreatedevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bc228-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc228-114">Sie müssen zuerst die debugschicht Direct3D 12 aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc228-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="bc228-115">Aktivieren Sie *anschließend* die directml-debugschicht durch Aufrufen von **dmlcreatedevice**.</span><span class="sxs-lookup"><span data-stu-id="bc228-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="bc228-116">Nachdem Sie die directml-Debugebene aktiviert haben, führen alle directml-Fehler oder ungültigen API-Aufrufe dazu, dass Debuginformationen als Debugausgabe ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc228-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="bc228-117">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="bc228-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="bc228-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc228-118">See also</span></span>

* [<span data-ttu-id="bc228-119">Dmlkreatedevice-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc228-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="bc228-120">Verfügbare Features: Bedarfs gesteuert</span><span class="sxs-lookup"><span data-stu-id="bc228-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="bc228-121">Verwenden der GPU-basierten Validierung mit der Direct3D 12-Debugebene</span><span class="sxs-lookup"><span data-stu-id="bc228-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="bc228-122">Direct3D 12-Debug-Ebenenverweis</span><span class="sxs-lookup"><span data-stu-id="bc228-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
