---
description: Sowohl Writer als auch Anforderer behalten die für einen Sicherungs-oder Wiederherstellungs Vorgang erforderlichen Informationen in ihren eigenen Metadatendokumenten.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: VSS-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350443"
---
# <a name="vss-metadata"></a><span data-ttu-id="26990-103">VSS-Metadaten</span><span class="sxs-lookup"><span data-stu-id="26990-103">VSS Metadata</span></span>

<span data-ttu-id="26990-104">Sowohl Writer als auch Anforderer behalten die für einen Sicherungs-oder Wiederherstellungs Vorgang erforderlichen Informationen in ihren eigenen Metadatendokumenten.</span><span class="sxs-lookup"><span data-stu-id="26990-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="26990-105">Diese Dokumente, das [*Writer-Metadatendokument*](vssgloss-w.md) und das [*Sicherungs Komponenten Dokument*](vssgloss-b.md), werden als Grundlage für die Kommunikation und Koordination von Writer und Anforderer während der Sicherungs-und Wiederherstellungs Aktivitäten verwendet.</span><span class="sxs-lookup"><span data-stu-id="26990-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="26990-106">Die Metadaten werden im XML-Format mithilfe eines proprietären Schemas dargestellt.</span><span class="sxs-lookup"><span data-stu-id="26990-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="26990-107">Metadaten können auf einen Datenträger, ein Band oder ein beliebiges anderes Massen Speichergerät kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="26990-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="26990-108">Er sollte bei einem Sicherungs Vorgang immer auf dem Sicherungsmedium gespeichert werden und muss im Verlauf eines Wiederherstellungs Vorgangs von diesem Medium abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="26990-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="26990-109">**Vorsicht:** Die spezifischen Details des Formats und des Schemas sind nur für die Verwendung durch das System vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="26990-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="26990-110">Entwickler sollten nicht versuchen, die XML-Darstellung der Metadaten zu ändern oder direkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26990-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="26990-111">Writer und Anforderer verfügen über eine Vielzahl von Abfrage-und Set-Methoden für den Zugriff auf und die Änderung der Sicherungs Komponenten und Writer-Metadatendokumente:</span><span class="sxs-lookup"><span data-stu-id="26990-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="26990-112">Arbeiten mit dem Writer-Metadatendokument</span><span class="sxs-lookup"><span data-stu-id="26990-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="26990-113">Arbeiten mit dem Dokument mit den Sicherungs Komponenten</span><span class="sxs-lookup"><span data-stu-id="26990-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="26990-114">VSS-Metadatenkomponenten</span><span class="sxs-lookup"><span data-stu-id="26990-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



