---
description: Befehle
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Befehle (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214542"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="fba10-103">Befehle (WPD-API)</span><span class="sxs-lookup"><span data-stu-id="fba10-103">Commands (WPD API)</span></span>

<span data-ttu-id="fba10-104">Die Client Anwendung und der Treiber kommunizieren mithilfe von Befehlen, die vom Client (über die Portable Windows-Geräte-API) an den Treiber gesendet werden (über das User-Mode Driver-Framework).</span><span class="sxs-lookup"><span data-stu-id="fba10-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="fba10-105">Ein Befehl kann einen-Parameter enthalten, und er kann ein-Ergebnis zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fba10-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="fba10-106">Ein Client kann einen Befehl explizit senden, indem er entweder die [**iportabledevice:: sendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) -Methode oder die **iportabledeviceservice: sendCommand** -Methode oder implizit durch Aufrufen einer der Methoden der Client Schnittstellen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fba10-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="fba10-107">Einige Befehle können nur explizit gesendet werden. Diese sind in der Dokumentation des Befehls angegeben.</span><span class="sxs-lookup"><span data-stu-id="fba10-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="fba10-108">Die Referenzseiten des Befehls beschreiben den Zweck eines Befehls sowie die Parameter, die erwartet werden sollen, und die Parameter, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fba10-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="fba10-109">Ein Befehl wird durch eine **PropertyKey** -Struktur identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fba10-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="fba10-110">Dies besteht aus zwei Teilen: einem GUID-Teil (dem *fmtid* -Member) und einem DWORD-Teil (dem *PID* -Member).</span><span class="sxs-lookup"><span data-stu-id="fba10-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="fba10-111">Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der der Befehl gehört (verwandte Befehle gehören derselben Kategorie an und verfügen daher über dieselbe *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="fba10-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="fba10-112">Der DWORD-Teil gibt die Befehls-ID an und wird verwendet, um die einzelnen Befehle innerhalb einer Befehls Kategorie zu unterscheiden (die *PID* -Werte für Befehle in derselben Kategorie werden unterschiedlich sein).</span><span class="sxs-lookup"><span data-stu-id="fba10-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="fba10-113">In der folgenden Tabelle werden die Kategorien von Befehlen aufgelistet, die von Windows-tragbaren Geräten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fba10-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="fba10-114">Gerätehersteller können eigene Befehle definieren, indem Sie Ihre eigenen Befehls Kategorien und Befehls-IDs erstellen.</span><span class="sxs-lookup"><span data-stu-id="fba10-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="fba10-115">Ein Hersteller sollte jedoch keine Befehle zu den unten aufgeführten Kategorien hinzufügen, da diese von Microsoft reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="fba10-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="fba10-116">**Befehls Kategorien**</span><span class="sxs-lookup"><span data-stu-id="fba10-116">**Command Categories**</span></span>



| <span data-ttu-id="fba10-117">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="fba10-117">Command category</span></span>                         | <span data-ttu-id="fba10-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba10-119">**Allgemeine WPD- \_ Kategorie \_**</span><span class="sxs-lookup"><span data-stu-id="fba10-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="fba10-120">Befehle, die allen Objekten und Geräten gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="fba10-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="fba10-121">**WPD- \_ Kategorie \_ Geräte \_ Hinweise**</span><span class="sxs-lookup"><span data-stu-id="fba10-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="fba10-122">Befehle, die zum Abrufen Optionaler Geräteinformationen verwendet werden, die verwendet werden können, um die Endbenutzer Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="fba10-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="fba10-123">**WPD- \_ Kategorie \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="fba10-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="fba10-124">Befehle, die für Geräte verwendet werden, die die SMS (Short Message Service)-Funktionalität unterstützen, die in der Regel auf Mobiltelefonen verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="fba10-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="fba10-125">**WPD- \_ Kategorie \_ trotzdem \_ Image \_ Erfassung**</span><span class="sxs-lookup"><span data-stu-id="fba10-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="fba10-126">Befehle, die für Geräte verwendet werden, die die Image Erfassung noch unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fba10-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="fba10-127">**WPD \_ - \_ kategoriespeicher**</span><span class="sxs-lookup"><span data-stu-id="fba10-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="fba10-128">Befehle, die für Speicher funktionale Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fba10-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="fba10-129">Die spezifischen Befehle, die für jeden dieser Typen definiert sind, werden in den folgenden Tabellen nach Befehlstyp organisiert angegeben.</span><span class="sxs-lookup"><span data-stu-id="fba10-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="fba10-130">**Kategorie "Kategorie Allgemein" in WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fba10-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="fba10-131">Get-Help</span><span class="sxs-lookup"><span data-stu-id="fba10-131">Command</span></span>                                                                                | <span data-ttu-id="fba10-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="fba10-133">**gemeinsamer WPD- \_ Befehl \_ \_ Gerät zurücksetzen \_**</span><span class="sxs-lookup"><span data-stu-id="fba10-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="fba10-134">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="fba10-134">Resets the device.</span></span> |



 

<span data-ttu-id="fba10-135">**Kategorie " \_ \_ Geräte \_ Hinweise" der WPD-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="fba10-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="fba10-136">Get-Help</span><span class="sxs-lookup"><span data-stu-id="fba10-136">Command</span></span>                                                                                                              | <span data-ttu-id="fba10-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="fba10-138">**gerätehinweise zum WPD- \_ Befehl \_ \_ \_ get \_ Content \_ Location**</span><span class="sxs-lookup"><span data-stu-id="fba10-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="fba10-139">Ruft die Objekt-IDs der Ordner ab, die ein Objekt eines angegebenen Typs enthalten können.</span><span class="sxs-lookup"><span data-stu-id="fba10-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="fba10-140">**Kategorie \_ \_ Speicher Kategorie für WPD**</span><span class="sxs-lookup"><span data-stu-id="fba10-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="fba10-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="fba10-141">Command</span></span>                                                                     | <span data-ttu-id="fba10-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="fba10-143">**WPD- \_ Befehls \_ Speicher- \_ eject**</span><span class="sxs-lookup"><span data-stu-id="fba10-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="fba10-144">Ewirft ein Speichermedium ein, das per Remote Zugriff vom Treiber entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fba10-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="fba10-145">**\_ \_ Speicher \_ Format für WPD-Befehl**</span><span class="sxs-lookup"><span data-stu-id="fba10-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="fba10-146">Formatiert ein Speicher funktionales Objekt auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="fba10-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="fba10-147">**Kategorie der Kategorie "WPD" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fba10-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="fba10-148">Get-Help</span><span class="sxs-lookup"><span data-stu-id="fba10-148">Command</span></span>                                                         | <span data-ttu-id="fba10-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="fba10-150">**WPD- \_ Befehl \_ SMS \_ senden**</span><span class="sxs-lookup"><span data-stu-id="fba10-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="fba10-151">Initiiert das Senden einer SMS-Nachricht durch ein SMS-Funktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="fba10-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="fba10-152">**Kategorie der WPD- \_ Kategorie \_ immer noch \_ Bild \_ Erfassung**</span><span class="sxs-lookup"><span data-stu-id="fba10-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="fba10-153">Get-Help</span><span class="sxs-lookup"><span data-stu-id="fba10-153">Command</span></span>                                                                                                   | <span data-ttu-id="fba10-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba10-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="fba10-155">**WPD- \_ Befehl wird \_ immer noch \_ \_ \_ initiiert**</span><span class="sxs-lookup"><span data-stu-id="fba10-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="fba10-156">Initiiert eine immer noch Bild Erfassung durch ein noch Bild funktionales Objekt.</span><span class="sxs-lookup"><span data-stu-id="fba10-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fba10-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fba10-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fba10-158">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="fba10-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



