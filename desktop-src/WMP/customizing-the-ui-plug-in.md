---
title: Anpassen des Plug-Ins für die Benutzeroberfläche
description: Anpassen des Plug-Ins für die Benutzeroberfläche
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Windows Media Player-Plug-ins, anpassen
- Plug-ins, anpassen
- Plug-Ins für die Benutzeroberfläche, anpassen
- UI-Plug-ins, anpassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037371"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="f5c59-107">Anpassen des Plug-Ins für die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f5c59-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="f5c59-108">An diesem Punkt ist Ihr Projekt bereit für die Anpassung.</span><span class="sxs-lookup"><span data-stu-id="f5c59-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="f5c59-109">Sie können die vom Assistenten generierte Implementierung der **iwmppluginui** -Schnittstelle ändern, Sie können der **cpluginwindow** -Klasse eine Benutzeroberfläche hinzufügen, und Sie können eine Eigenschaften Seite in der **cpropertydialog** -Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="f5c59-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="f5c59-110">Wenn das Plug-in für das Lauschen auf Windows Media Player-Ereignisse konfiguriert ist, werden vom Assistenten standardmäßige oder leere Implementierungen aller erforderlichen Ereignishandler generiert, die Sie ebenfalls ändern oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5c59-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="f5c59-111">Der Typ des Plug-ins und die von ihm unterstützten Funktionen werden durch einen Wert angezeigt, der in der Windows-Registrierung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5c59-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="f5c59-112">Der Assistent generiert eine Datei mit der Dateinamenerweiterung RGS, die die Informationen enthält, mit denen das Plug-in registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5c59-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="f5c59-113">Der "Funktionen"-Wert in dieser Datei ist die dezimale Entsprechung eines booleschen Werts oder der Plug-in-Typkonstanten und Plug-in-Flags, die in "wmpplug. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f5c59-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="f5c59-114">Obwohl dieser Wert durch die Optionen bestimmt wird, die Sie im Assistenten auswählen, müssen Sie ihn ändern, wenn Sie ein Plug-in mit mehreren Voreinstellungen erstellen möchten oder eine, an die Medienelemente oder Wiedergabelisten gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f5c59-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="f5c59-115">Wenn Sie Ihren Plug-in-Code ändern und erweitern, können Sie die dll erstellen und registrieren, damit Sie Ihr Plug-in in Windows Media Player testen können.</span><span class="sxs-lookup"><span data-stu-id="f5c59-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5c59-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5c59-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c59-117">**Aufbau eines UI-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="f5c59-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




