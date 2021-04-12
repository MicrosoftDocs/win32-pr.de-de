---
description: Die Volumeschattenkopie-Dienst (VSS)-API stellt sowohl com-als auch C++-Schnittstellen zur Unterstützung der Erstellung von Anforderern und Writern bereit.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Volumeschattenkopie-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129304"
---
# <a name="volume-shadow-copy-api-interfaces"></a>Volumeschattenkopie-API

Die Volumeschattenkopie-Dienst (VSS)-API stellt sowohl com-als auch C++-Schnittstellen zur Unterstützung der Erstellung von Anforderern und Writern bereit.

## <a name="vss-requester-specific-interfaces"></a>VSS-Requester-Specific Schnittstellen

-   [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [**Ivssbackupcomponentsex**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [**Ivssexamineschreibmetadaten**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [**IVssExamineWriterMetadataEx**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [**Ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [**Ivssschreitercomponentsxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a>VSS-Writer-Specific Schnittstellen

-   [**Ivsskreateexpressschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [**Ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [**Ivssexpresswriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [**Ivssschreitercomponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a>VSS-Hardware Provider-Specific Schnittstellen

-   [**Ivssadmin**](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [**Ivsshardwaresnapshotprovider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [**Ivsshardwaresnapshotproviderex**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [**Ivssproviderkreatesnapshotset**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [**Ivssprovidernotification**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a>VSS-Software Provider-Specific Schnittstellen

-   [**Ivsssoftwaresnapshotprovider**](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a>Freigegebene VSS-Schnittstellen

-   [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [**Ivsscomponstex**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [**Ivssenumuject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [**Ivsswmabhängigkeit**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [**Ivsswmfiledebug**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a>VSS-Verwaltungs Schnittstellen

-   [**Ivssdifferenalsoftwaresnapshotmgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [**Ivssenumschlag-gmtobject**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [**Ivsssnapshotmgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
