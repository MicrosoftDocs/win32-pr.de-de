---
title: Selbstregistrierung für Steuerelemente
description: Selbstregistrierung für Steuerelemente
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339299"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="730bc-103">Selbstregistrierung für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="730bc-103">Self Registration for Controls</span></span>

<span data-ttu-id="730bc-104">ActiveX-Steuerelemente müssen die Selbstregistrierung unterstützen, indem die Funktionen [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="730bc-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="730bc-105">ActiveX-Steuerelemente müssen alle Standard Registrierungseinträge für einbettbare Objekte und Automatisierungsserver registrieren.</span><span class="sxs-lookup"><span data-stu-id="730bc-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="730bc-106">ActiveX-Steuerelemente müssen die Komponenten Kategorien-API verwenden, um sich selbst als Steuerelement zu registrieren und die Komponenten Kategorien zu registrieren, die von einem Host unterstützt werden müssen, sowie alle Kategorien, die das Steuerelement implementiert, siehe [Komponenten Kategorien](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="730bc-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="730bc-107">ActiveX-Steuerelemente sollten auch den Registrierungsschlüssel [ToolBoxBitmap32](toolboxbitmap32.md) registrieren, obwohl dies nicht zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="730bc-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="730bc-108">Die Insertable-Komponenten Kategorie sollte nur registriert werden, wenn das Steuerelement als Verbund Dokument Objekt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="730bc-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="730bc-109">Es ist wichtig zu beachten, dass ein Verbund Dokument Objekt bestimmte Schnittstellen unterstützen muss, die über die für ein ActiveX-Steuerelement erforderlichen minimalen [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="730bc-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="730bc-110">Obwohl ein ActiveX-Steuerelement als Verbund Dokument Objekt qualifiziert sein kann, sollte die Dokumentation des Steuer Elements in den folgenden Situationen eindeutig angeben, welches Verhalten zu erwarten ist.</span><span class="sxs-lookup"><span data-stu-id="730bc-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="730bc-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="730bc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730bc-112">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="730bc-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 