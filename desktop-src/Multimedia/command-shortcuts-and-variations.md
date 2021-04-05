---
title: Befehls Verknüpfungen und Variationen
description: Befehls Verknüpfungen und Variationen
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712528"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="7dd87-103">Befehls Verknüpfungen und Variationen</span><span class="sxs-lookup"><span data-stu-id="7dd87-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="7dd87-104">Beim Arbeiten mit MCI-Befehlen können Sie mehrere Tastenkombinationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dd87-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="7dd87-105">Mit diesen Tastenkombinationen können Sie einen einzelnen Bezeichner verwenden, um auf alle Geräte zu verweisen, die Ihre Anwendung geöffnet hat, oder um ein Gerät zu öffnen, ohne explizit einen [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) auszugeben.</span><span class="sxs-lookup"><span data-stu-id="7dd87-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="7dd87-106">Sie können "All" (MCI \_ All \_ Device \_ ID) als Geräte Bezeichner für jeden Befehl angeben, der keine Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7dd87-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="7dd87-107">Wenn Sie "alle" angeben, sendet MCI den Befehl sequenziell an alle Geräte, die von der aktuellen Anwendung geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7dd87-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="7dd87-108">Beispielsweise schließt der Befehl "alle" [**Schließen**](close.md) alle geöffneten Geräte, und der Befehl "alle" Wiedergeben beginnt [**mit der wieder**](play.md) Gabe aller Geräte, die von der Anwendung geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7dd87-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="7dd87-109">Da MCI die Befehle sequenziell an die MCI-Geräte sendet, gibt es ein Intervall zwischen dem Zeitpunkt, an dem der erste und das letzte Gerät den Befehl erhalten.</span><span class="sxs-lookup"><span data-stu-id="7dd87-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="7dd87-110">Die Verwendung von "All" ist eine bequeme Möglichkeit, einen Befehl an alle Ihre Geräte zu übertragen, aber Sie sollten sich nicht darauf verlassen, dass Geräte synchronisiert werden. die zeitliche Steuerung zwischen Nachrichten kann variieren.</span><span class="sxs-lookup"><span data-stu-id="7dd87-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="7dd87-111">Wenn Sie einen Befehl ausgeben und ein Gerät angeben, das nicht geöffnet ist, versucht MCI, das Gerät zu öffnen, bevor der Befehl implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7dd87-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="7dd87-112">Die folgenden Regeln gelten für das automatische Öffnen von Geräten:</span><span class="sxs-lookup"><span data-stu-id="7dd87-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="7dd87-113">Das Feature für automatisches Öffnen funktioniert nur mit der Befehls Zeichenfolgen-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7dd87-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="7dd87-114">Die Funktion für automatisches Öffnen schlägt für Befehle fehl, die für benutzerdefinierte Gerätetreiber spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="7dd87-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="7dd87-115">Automatisch geöffnete Geräte Antworten nicht auf Befehle, die "All" als Gerätenamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dd87-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="7dd87-116">Die Funktion zum automatischen öffnen lässt die Anwendung das Flag "Type" nicht zu.</span><span class="sxs-lookup"><span data-stu-id="7dd87-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="7dd87-117">Ohne den Gerätenamen bestimmt MCI den Gerätenamen aus den Einträgen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7dd87-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="7dd87-118">Wenn Sie ein bestimmtes Gerät verwenden möchten, können Sie den Gerätenamen mit dem Dateinamen kombinieren, indem Sie das Ausrufezeichen verwenden, wie im Referenzmaterial für den Befehl " [**Öffnen**](open.md) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7dd87-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="7dd87-119">Wenn eine Anwendung das Feature für automatisches Öffnen zum Öffnen eines Geräts verwendet, sollte die Anwendung den Rückgabewert jedes nachfolgenden geöffneten Befehls überprüfen, um sicherzustellen, dass das Gerät noch geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="7dd87-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="7dd87-120">MCI schließt auch automatisch alle Geräte, die automatisch geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7dd87-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="7dd87-121">MCI schließt ein Gerät in der Regel in den folgenden Situationen:</span><span class="sxs-lookup"><span data-stu-id="7dd87-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="7dd87-122">Der Befehl ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7dd87-122">The command is completed.</span></span>
-   <span data-ttu-id="7dd87-123">Sie brechen den Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="7dd87-123">You abort the command.</span></span>
-   <span data-ttu-id="7dd87-124">Sie fordern eine Benachrichtigung in einem nachfolgenden Befehl an.</span><span class="sxs-lookup"><span data-stu-id="7dd87-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="7dd87-125">MCI erkennt einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7dd87-125">MCI detects a failure.</span></span>

 

 




