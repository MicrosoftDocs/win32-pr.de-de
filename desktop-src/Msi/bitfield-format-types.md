---
description: Die Bitfield-Format Typen konfigurierbarer Daten können in ganzzahligen Datenbankfeldern verwendet werden.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Bitfield-Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b443f7ee363d1a2b48eb580623018264df8d50be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358850"
---
# <a name="bitfield-format-types"></a>Bitfield-Format Typen

Die Bitfield-Format Typen konfigurierbarer Daten können in ganzzahligen Datenbankfeldern verwendet werden. Der Benutzer sollte einen Wert aus einer angegebenen Teilmenge auswählen. Dies erfolgt ausschließlich gemäß Konvention und wird von Mergemod.dll nicht erzwungen. Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.

Der folgende Bitfield-Formattyp ist vorhanden.

[Beliebiger Bitfeldtyp](arbitrary-bitfield-type.md)

Konfigurierbare Elemente des Bitfield-Formattyps werden in ganzzahligen Spalten verwendet und können im Allgemeinen durch eine beliebige ganze Zahl ersetzt werden. Der Benutzer sollte einen Wert aus einer angegebenen Teilmenge auswählen. Dies erfolgt ausschließlich gemäß Konvention und wird von Mergemod.dll nicht erzwungen. Der Autor sollte das Modul so vorbereiten, dass es jeden beliebigen Wert verarbeitet.

 

 



