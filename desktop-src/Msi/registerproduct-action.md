---
description: Die Aktion registerproduct registriert die Produktinformationen mit dem Installationsprogramm und mit der Option "Software". Außerdem wird mit dieser Aktion das Windows Installer-Daten Bank Paket auf dem lokalen Computer gespeichert.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Registerproduct-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373026"
---
# <a name="registerproduct-action"></a>Registerproduct-Aktion

Die Aktion registerproduct registriert die Produktinformationen mit dem Installationsprogramm und mit der Option "Software". Außerdem wird mit dieser Aktion das Windows Installer-Daten Bank Paket auf dem lokalen Computer gespeichert.

Mit der registerproduct-Aktion werden die Steuerelemente konfiguriert, die in der Systemsteuerung über die Option "Software" angezeigt werden. Weitere Informationen finden Sie unter [Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten            |
|-------|---------------------------------------|
| \[1\] | Informationen zu registriertes Produkt. |



 

## <a name="remarks"></a>Bemerkungen

Die Aktion "registerproduct" wird während der Installation nicht an einem administrativen Installations Punkt ausgeführt.

 

 



