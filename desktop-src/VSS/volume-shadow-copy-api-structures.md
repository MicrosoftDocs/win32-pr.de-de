---
description: Die folgenden Strukturen sind in der Volumeschattenkopie-API definiert.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Volumen Schatten Kopie-API-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1bb699277faa30c6a570203cd820d552cc9f1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346949"
---
# <a name="volume-shadow-copy-api-structures"></a>Volumen Schatten Kopie-API-Strukturen

Die folgenden Strukturen sind in der Volumeschattenkopie-API definiert.



| Struktur                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Enthält Informationen zu einer bestimmten Komponente.                                                                                                                                                                                                                       |
| [**VSS- \_ diff- \_ Bereichs- \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Beschreibt Zuordnungen zwischen Quellvolumes mit den ursprünglichen Datei Daten und Volumes, die den Schattenkopiespeicherbereich enthalten.                                                                                                                                |
| [**VSS- \_ diff- \_ \_ volumeprop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Beschreibt ein schattenkopiespeichervolume.                                                                                                                                                                                                                        |
| [**VSS- \_ Mgmt- \_ Objekt- \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Beschreibt die Eigenschaften eines Volumes, eines schattenkopiespeichervolumes oder eines Schattenkopiespeicherbereichs.                                                                                                                                                                    |
| [**VSS- \_ Mgmt- \_ Objekt \_ Union**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Eine Union of [**VSS \_ Volume \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), [**VSS \_ diff \_ Volume \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)und [**VSS \_ diff \_ Area \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) -Strukturen, die von der [**VSS- \_ Mgmt-Objekt- \_ \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) -Struktur verwendet werden. |
| [**VSS- \_ Objekt- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Beschreibt die Eigenschaften eines Anbieters, eines Volumes, einer Schatten Kopie oder einer Schattenkopiesatz.                                                                                                                                                                                    |
| [**VSS- \_ Objekt \_ Union**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Eine Union der VSS- [**\_ Momentaufnahme \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -und [**VSS-Anbieter- \_ \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) -Strukturen, die von der [**VSS-Objekt- \_ \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) -Struktur verwendet werden                                                                    |
| [**VSS- \_ Anbieter- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Gibt Eigenschaften von schattenkopieanbietern an.                                                                                                                                                                                                                          |
| [**VSS- \_ Momentaufnahme- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Enthält die Eigenschaften einer Schatten Kopie oder eines schattenkopiesatzes.                                                                                                                                                                                                        |
| [**VSS \_ - \_ volumeprop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Beschreibt die Eigenschaften eines schattenkopiequellvolumes.                                                                                                                                                                                                            |
| [**VSS \_ - \_ \_ volumeschutzinformationen**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Enthält Informationen über die schattenkopieschutzebene eines Volumes.                                                                                                                                                                                                 |



 

 

 



