---
description: Die ganzzahligen Format Typen konfigurierbarer Daten können entweder in Text-oder ganzzahligen Datenbankfeldern verwendet werden. Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Ganzzahlige Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757033"
---
# <a name="integer-format-types"></a>Ganzzahlige Format Typen

Die ganzzahligen Format Typen konfigurierbarer Daten können entweder in Text-oder ganzzahligen Datenbankfeldern verwendet werden. Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.

Der folgende ganzzahlige Formattyp ist vorhanden.

[Beliebiger Integer-Typ](arbitrary-integer-type.md)

Konfigurierbare Elemente des ganzzahligen Formattyps werden in Text-oder ganzzahligen Spalten verwendet und können im Allgemeinen durch eine beliebige positive oder negative ganze Zahl ersetzt werden. Bestimmte konfigurierbare Elemente können jedoch auch über charakteristische Semantik Einschränkungen verfügen. Beispielsweise weist ein bestimmtes konfigurierbares Element, das eine ganze Zahl zwischen 0 und 100 sein muss, eine zusätzliche semantische Einschränkung auf. Solche Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die den angegebenen ganzzahligen Formattyp erfüllt.

 

 



