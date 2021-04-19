---
description: Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, mit dem eine Windows-Anwendung XPS-Dokument Dateien (XML Paper Specification) in Windows-Versionen ab Windows XP mit Service Pack 2 (SP2) erstellen kann.
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353963"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="4348b-103">Microsoft XPS Document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="4348b-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="4348b-104">Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, mit dem eine Windows-Anwendung XPS-Dokument Dateien (XML Paper Specification) in Windows-Versionen ab Windows XP mit Service Pack 2 (SP2) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4348b-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="4348b-105">Die Verwendung von MXDW ermöglicht es einer Windows-Anwendung, den Inhalt als XPS-Dokument zu speichern, ohne den Programmcode der Anwendung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4348b-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4348b-106">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="4348b-106">When to Use</span></span>

<span data-ttu-id="4348b-107">Als Benutzer wählen Sie das MXDW aus, wenn Sie ein XPS-Dokument aus einer Windows-Anwendung erstellen möchten, die nicht über die Option zum Speichern des Inhalts als XPS-Dokument verfügt.</span><span class="sxs-lookup"><span data-stu-id="4348b-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="4348b-108">Als Anwendungsentwickler empfiehlt es sich, MXDW für Benutzer zu empfehlen, die XPS-Dokumente erstellen möchten, wenn Ihre Anwendung nicht die Option zum Speichern als XPS-Dokument bietet.</span><span class="sxs-lookup"><span data-stu-id="4348b-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="4348b-109">Weitere Informationen zu XML Paper Specification und XPS-Dokumenten finden Sie unter [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) und [XPS Specification und Lizenz Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="4348b-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="4348b-110">MXDW wird automatisch unter Windows Vista und höheren Versionen von Windows installiert und kann unter Windows XP mit SP2 und Windows Server 2003 heruntergeladen und installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4348b-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="4348b-111">Installation</span><span class="sxs-lookup"><span data-stu-id="4348b-111">Installation</span></span>

<span data-ttu-id="4348b-112">Unter Windows Vista und höheren Versionen von Windows wird MXDW bei der Installation des Betriebssystems automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="4348b-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="4348b-113">**Windows XP mit SP2 und Windows Server 2003**: Laden Sie entweder .NET Framework 3,0 oder das XPS Essentials Pack aus dem [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx)herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="4348b-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="4348b-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="4348b-114">How to Use</span></span>

<span data-ttu-id="4348b-115">Bei der Installation wird MXDW als verfügbare Druck Warteschlange im Dialogfeld Drucken angezeigt, das von einer Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4348b-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="4348b-116">Wenn MXDW als Drucker ausgewählt ist, wird der Benutzer aufgefordert, den Dateinamen zu erstellen, der als XPS-Dokument erstellt wird, das die Ausgabe der Anwendung erfasst.</span><span class="sxs-lookup"><span data-stu-id="4348b-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="4348b-117">Die folgende Abbildung zeigt, wie MXDW im Dialogfeld allgemeiner Druck von Windows Vista als Drucker ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4348b-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![ein Bild des Dialog Felds drucken, das die Auswahl von Microsoft XPS Document Writer (MXDW) anzeigt.](images/choosingmxdwinvista.gif)

<span data-ttu-id="4348b-119">Anwendungsentwickler können die Ausgabe von MXDW mithilfe der [MXDW-Konfigurationseinstellungen](mxdw-configuration-settings.md)anpassen.</span><span class="sxs-lookup"><span data-stu-id="4348b-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4348b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4348b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4348b-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4348b-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="4348b-122">XPS-Spezifikation und Lizenz Downloads</span><span class="sxs-lookup"><span data-stu-id="4348b-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="4348b-123">[isXPS-Konformitäts Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4348b-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4348b-124">MXDW-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="4348b-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
