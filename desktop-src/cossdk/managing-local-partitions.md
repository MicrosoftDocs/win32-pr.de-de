---
description: Als Alternative zum Erstellen und Konfigurieren lokaler Partitionen über das Verwaltungstool komponentendienste können Sie Partitionen programmgesteuert verwalten, indem Sie partitionsspezifische COM+-Verwaltungssammlungen und -Eigenschaften verwenden.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Verwalten lokaler Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124d0b9ef7bf54f07a6b28561428c57834a6e15ec11c4ed5c89fb92f95f0a950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306243"
---
# <a name="managing-local-partitions"></a>Verwalten lokaler Partitionen

Als Alternative zum Erstellen und Konfigurieren lokaler Partitionen über das Verwaltungstool komponentendienste können Sie Partitionen programmgesteuert verwalten, indem Sie partitionsspezifische COM+-Verwaltungssammlungen und -Eigenschaften verwenden.

> [!Note]  
> Der COM+-Partitionsdienst ist standardmäßig nicht aktiviert. Um den COM+-Partitionsdienst verwenden zu können, müssen Sie ihn über das Verwaltungstool komponentendienste oder durch Ändern der PartitionsEnabled-Eigenschaft in der [**LocalComputer-Sammlung**](localcomputer.md) in True aktivieren.

 

Die folgende Unterroutine, die in Visual Basic-Skript geschrieben wurde, veranschaulicht, wie eine Partition auf dem lokalen Computer erstellt wird:


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



Die folgende Unterroutine, die in Visual Basic-Skript geschrieben wurde, veranschaulicht, wie eine Partition vom lokalen Computer gelöscht wird:


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



Die folgende Unterroutine, die in Visual Basic-Skript geschrieben wurde, veranschaulicht, wie die Standardpartition für einen Benutzer festgelegt wird:


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



Die folgende Unterroutine, die in Visual Basic-Skript geschrieben wurde, veranschaulicht, wie die Standardpartition für einen Benutzer entfernt wird:


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitionsmetriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitionscaches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



