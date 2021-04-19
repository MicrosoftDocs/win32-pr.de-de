---
description: Beschreibt den Prozess des erbauens einer WSDAPI-Anwendung mithilfe von wsdcodegen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Verwenden von wsdcodegen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350247"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="a1614-103">Verwenden von wsdcodegen</span><span class="sxs-lookup"><span data-stu-id="a1614-103">Using WsdCodeGen</span></span>

<span data-ttu-id="a1614-104">**So erstellen Sie eine WSDAPI-Anwendung mithilfe von wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="a1614-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="a1614-105">Definieren Sie den funktionalen Vertrag für den Geräte Host in einer WSDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="a1614-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="a1614-106">Generieren Sie eine Konfigurationsdatei mithilfe von wsdcodegen.</span><span class="sxs-lookup"><span data-stu-id="a1614-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="a1614-107">Weitere Informationen finden Sie unter [wsdcodegen-Konfigurationsdatei](wsdcodegen-configuration-file.md) und [Befehlszeilen Syntax von wsdcodegen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a1614-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="a1614-108">Öffnen Sie die generierte Konfigurationsdatei, und ändern Sie die Datei nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="a1614-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="a1614-109">Wenn Sie eine Client Anwendung entwickeln, sind nur wenige oder gar keine Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1614-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="a1614-110">Wenn Sie eine Host Anwendung entwickeln, ändern Sie die benutzerspezifischen Konfigurationselemente (z. b. [**Hersteller**](manufacturer.md) und [**modelname**](modelname.md)).</span><span class="sxs-lookup"><span data-stu-id="a1614-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="a1614-111">Generieren Sie mithilfe von wsdcodegen Code, und geben Sie die Konfigurationsdatei als Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="a1614-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="a1614-112">Weitere Informationen finden Sie unter [Befehlszeilen Syntax von wsdcodegen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a1614-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="a1614-113">Verwenden Sie den generierten Code zum Erstellen eines Clients, Hosts oder beides.</span><span class="sxs-lookup"><span data-stu-id="a1614-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="a1614-114">Die Windows SDK umfasst einige WSDL-Beispieldateien, wsdcodegen-Konfigurationsdateien und generierten Code.</span><span class="sxs-lookup"><span data-stu-id="a1614-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="a1614-115">Weitere Informationen finden Sie unter [WSDAPI Samples](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a1614-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1614-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1614-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1614-117">WSDAPI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1614-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



