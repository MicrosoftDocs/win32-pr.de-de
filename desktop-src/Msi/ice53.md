---
description: ICE53 prüft Einträge in der Registrierungs Tabelle, die Informationen zum privaten Installer oder Richtlinien Werte in die Systemregistrierung schreiben.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350798"
---
# <a name="ice53"></a>ICE53

ICE53 prüft Einträge in der Registrierungs Tabelle, die Informationen zum privaten Installer oder Richtlinien Werte in die Systemregistrierung schreiben.

## <a name="result"></a>Ergebnis

ICE53 gibt eine Warnung aus, wenn in der Registrierungs Tabelle das Schreiben interner oder Richtlinien Informationen in die Registrierung angegeben ist.

## <a name="example"></a>Beispiel

ICE53 gibt die folgende Warnung für das gezeigte Beispiel aus.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung             | Root         | Schlüssel                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **DISABLEROLLBACK**<br/> |



 

In der Registrierungs Tabellenzeile "Registry1" wird ein Systemrichtlinien Wert in die Registrierung geschrieben, der sich auf die Installation aller Pakete auswirkt. Abhängig vom Paket kann es möglich sein, das Rollback für dieses Paket allein zu deaktivieren, indem die [**DISABLEROLLBACK**](-disablerollback.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)festgelegt wird. Siehe [Rollback-Installation](rollback-installation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




