---
description: Nachdem für die Warteschlange ein Commit erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Aktualisieren von Registrierungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960441"
---
# <a name="updating-registry-information"></a><span data-ttu-id="7a2cb-103">Aktualisieren von Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="7a2cb-103">Updating Registry Information</span></span>

<span data-ttu-id="7a2cb-104">Nachdem für die Warteschlange ein Commit erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="7a2cb-105">Es wird empfohlen, dass Sie warten, bis alle erforderlichen Datei Kopiervorgänge erfolgreich abgeschlossen wurden, bevor Sie Registrierungsinformationen ändern.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="7a2cb-106">Eine Möglichkeit zum Aktualisieren der Registrierung besteht darin, [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) mit den angegebenen spinst- \_ Dateien, spinst \_ Registry oder spinst \_ INI2REG Flags aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="7a2cb-107">Diese Flags können in einem Befehl von **setupinstallfrominfsection** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="7a2cb-108">Im folgenden Beispiel wird spinst \_ all ^ spinst- \_ Dateien verwendet, um anzugeben, dass die-Funktion alle aufgelisteten Vorgänge mit Ausnahme von Datei Vorgängen verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="7a2cb-109">Da nur ini-, Registrierungs-und Datei Vorgänge im **Installations** Abschnitt aufgeführt sind, ist dies eine Kurzmethode, um anzugeben, dass die-Funktion alle ini-und Registrierungs Vorgänge verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="7a2cb-110">Im folgenden Beispiel wird gezeigt, wie Registrierungsinformationen mithilfe der **setupinstallfrominfsection** -Funktion installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="7a2cb-111">Im Beispiel ist "Besitzer *Window* " **null** , da nur Datei Vorgänge Dialogfelder generieren und somit kein übergeordnetes Fenster benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="7a2cb-112">"Myinf" ist die INF-Datei, die den zu verarbeitenden Abschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="7a2cb-113">Der Parameter "mySection" gibt den zu installierenden Abschnitt an.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="7a2cb-114">Die kombinierten Flags, spinst \_ alle ^ spinst- \_ Dateien, geben an, welche Installations Vorgänge verarbeitet werden sollen, in diesem Fall alle Vorgänge mit Ausnahme von Datei Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="7a2cb-115">Der Quell Stamm Pfad wird als "A: \\ " angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="7a2cb-116">Da keine Kopiervorgänge verarbeitet werden, werden die Parameter " *copyflags*", " *msghandler*", " *context*", " *deviceinfoset*" und " *deviceinfodata* " nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a2cb-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



