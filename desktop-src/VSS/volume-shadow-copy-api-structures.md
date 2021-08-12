---
description: Die folgenden Strukturen werden in der Volumeschattenkopie-API definiert.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Volumeschattenkopie-API-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590552"
---
# <a name="volume-shadow-copy-api-structures"></a>Volumeschattenkopie-API-Strukturen

Die folgenden Strukturen werden in der Volumeschattenkopie-API definiert.



| Struktur                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Enthält Informationen zu einer bestimmten Komponente.                                                                                                                                                                                                                       |
| [**VSS \_ DIFF \_ AREA \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Beschreibt Zuordnungen zwischen Quellvolumes, die die ursprünglichen Dateidaten enthalten, und Volumes, die den Schattenkopiespeicherbereich enthalten.                                                                                                                                |
| [**VSS \_ DIFF \_ VOLUME \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Beschreibt ein Schattenkopie-Speicherbereichsvolumen.                                                                                                                                                                                                                        |
| [**VSS \_ MGMT \_ OBJECT \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Beschreibt die Eigenschaften eines Volumes, eines Schattenkopie-Speichervolumens oder eines Schattenkopiespeicherbereichs.                                                                                                                                                                    |
| [**VSS \_ MGMT \_ OBJECT \_ UNION**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Eine Vereinigung von [**VSS \_ VOLUME \_ PROP-,**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop) [**VSS \_ DIFF VOLUME \_ \_ PROP-**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)und [**VSS DIFF AREA \_ \_ \_ PROP-Strukturen,**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) die von der [**VSS \_ MGMT OBJECT \_ \_ PROP-Struktur verwendet**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) werden. |
| [**VSS \_ OBJECT \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Beschreibt die Eigenschaften eines Anbieters, Volumes, einer Schattenkopie oder eines Schattenkopiesets.                                                                                                                                                                                    |
| [**VSS \_ OBJECT \_ UNION**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Eine Union von [**VSS \_ SNAPSHOT \_ PROP-**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) und [**VSS \_ PROVIDER \_ PROP-Strukturen,**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) die von der [**VSS OBJECT \_ \_ PROP-Struktur verwendet**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) werden.                                                                    |
| [**VSS \_ PROVIDER \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Gibt Eigenschaften des Schattenkopieanbieters an.                                                                                                                                                                                                                          |
| [**VSS \_ SNAPSHOT \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Enthält die Eigenschaften einer Schattenkopie oder eines Schattenkopiesets.                                                                                                                                                                                                        |
| [**VSS \_ VOLUME \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Beschreibt die Eigenschaften eines Schattenkopie-Quellvolumens.                                                                                                                                                                                                            |
| [**\_ \_ VSS-VOLUMESCHUTZINFORMATIONEN \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Enthält Informationen zur Schutzebene für Schattenkopien eines Volumes.                                                                                                                                                                                                 |



 

 

 



