---
description: ICE53 sucht nach Einträgen in der Registrierungstabelle, die Informationen zum privaten Installationsprogramm oder Richtlinienwerte in die Systemregistrierung schreiben.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635131"
---
# <a name="ice53"></a>ICE53

ICE53 sucht nach Einträgen in der Registrierungstabelle, die Informationen zum privaten Installationsprogramm oder Richtlinienwerte in die Systemregistrierung schreiben.

## <a name="result"></a>Ergebnis

ICE53 gibt eine Warnung aus, wenn die Registrierungstabelle angibt, dass interne oder Richtlinieninformationen in die Registrierung geschrieben werden.

## <a name="example"></a>Beispiel

ICE53 gibt die folgende Warnung für das gezeigte Beispiel aus.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Registrierungstabelle](registry-table.md) (partiell)



| Registrierung             | Root         | Key                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installationsprogramm** \\ **DisableRollback**<br/> |



 

Die Registrierungstabellenzeile "Registry1" schreibt einen Systemrichtlinienwert in die Registrierung, der sich auf die Installation aller Pakete auswirkt. Je nach Paket kann es möglich sein, das Rollback für dieses Paket allein durch Festlegen der [**DISABLEROLLBACK-Eigenschaft**](-disablerollback.md) in der [Property-Tabelle](property-table.md)zu deaktivieren. Weitere Informationen finden Sie unter [Rollbackinstallation.](rollback-installation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




