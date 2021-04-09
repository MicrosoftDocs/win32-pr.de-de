---
description: Als Alternative zum Erstellen und Konfigurieren lokaler Partitionen über das Verwaltungs Programmkomponenten Dienste können Sie Partitionen Programm gesteuert verwalten, indem Sie Partitions spezifische com+-Verwaltungs Sammlungen und-Eigenschaften verwenden.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Verwalten von lokalen Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958567"
---
# <a name="managing-local-partitions"></a>Verwalten von lokalen Partitionen

Als Alternative zum Erstellen und Konfigurieren lokaler Partitionen über das Verwaltungs Programmkomponenten Dienste können Sie Partitionen Programm gesteuert verwalten, indem Sie Partitions spezifische com+-Verwaltungs Sammlungen und-Eigenschaften verwenden.

> [!Note]  
> Der com+-Partitions Dienst ist standardmäßig nicht aktiviert. Um den com+-Partitions Dienst zu verwenden, müssen Sie ihn über das Verwaltungs Tool Komponenten Dienste oder durch Ändern der partitionsenabled-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung auf true aktivieren.

 

Die folgende Unterroutine, die in Visual Basic Skript geschrieben wurde, veranschaulicht das Erstellen einer Partition auf dem lokalen Computer:


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



Die folgende Unterroutine, die in Visual Basic Skript geschrieben wurde, veranschaulicht, wie eine Partition vom lokalen Computer gelöscht wird:


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



Die folgende Unterroutine, die in Visual Basic Skript geschrieben wurde, veranschaulicht, wie die Standard Partition für einen Benutzer festgelegt wird:


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



Die folgende Unterroutine, die in Visual Basic Skript geschrieben wurde, veranschaulicht, wie die Standard Partition für einen Benutzer entfernt wird:


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

[Sammeln von Partitions Metriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitions Caches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



