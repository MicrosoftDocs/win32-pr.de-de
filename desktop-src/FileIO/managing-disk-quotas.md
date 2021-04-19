---
description: Administratoren können die Menge der Daten steuern, die von den einzelnen Benutzern auf einem NTFS-Dateisystem Volume gespeichert werden können.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Verwalten der Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363719"
---
# <a name="managing-disk-quotas"></a>Verwalten der Datenträger Kontingente

Das NTFS-Dateisystem unterstützt Datenträger *Kontingente*, mit denen Administratoren die Menge der Daten steuern können, die von den einzelnen Benutzern auf einem NTFS-Dateisystem Volume gespeichert werden können. Administratoren können das System optional so konfigurieren, dass ein Ereignis protokolliert wird, wenn sich Benutzer in Ihrer Nähe befinden, und den Benutzern, die ihr Kontingent überschreiten, weiteren Speicherplatz verweigern. Administratoren können auch Berichte generieren und mit dem Ereignis Monitor Kontingent Probleme nachverfolgen.

Sie können bestimmen, ob ein Dateisystem Datenträger Kontingente unterstützt, indem Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das Bitflag für die **Datei \_ Volumen \_ Kontingente** untersuchen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verwaltung von Datenträger Kontingenten auf Benutzerebene](user-level-administration-of-disk-quotas.md)<br/>     | So erhalten Sie mehr freien Speicherplatz, nachdem Sie das Kontingent Kontingent überschritten haben.<br/>                                                                  |
| [Verwaltung von Datenträger Kontingenten auf System Ebene](system-level-administration-of-disk-quotas.md)<br/> | Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standard Kontingente für das Volume festlegen.<br/> |
| [Limits für Datenträger Kontingente](disk-quota-limits.md)<br/>                                                   | Beschreibt zwei Arten von Datenträger Kontingent Limits und wie die Datenträger Kontingent Limits gemessen werden.<br/>                                                      |
| [Schnittstellen für Festplattenkontingente](disk-quota-interfaces.md)<br/>                                           | Mit Datenträger Kontingenten verwendete Schnittstellen.<br/>                                                                                                     |



 

 

 




