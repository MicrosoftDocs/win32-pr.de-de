---
description: Die Ganzzahlformattypen konfigurierbarer Daten können entweder in Text- oder ganzzahligen Datenbankfeldern verwendet werden. Das msmConfigItemNonNullable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Ganzzahlige Formattypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805628"
---
# <a name="integer-format-types"></a>Ganzzahlige Formattypen

Die Ganzzahlformattypen konfigurierbarer Daten können entweder in Text- oder ganzzahligen Datenbankfeldern verwendet werden. Das msmConfigItemNonNullable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.

Der folgende Ganzzahlformattyp ist vorhanden.

[Beliebiger ganzzahliger Typ](arbitrary-integer-type.md)

Konfigurierbare Elemente des Ganzzahlformattyps werden entweder in Text- oder ganzzahligen Spalten verwendet und können im Allgemeinen durch eine positive oder negative ganze Zahl ersetzt werden. Bestimmte konfigurierbare Elemente können jedoch auch charakteristische semantische Einschränkungen haben. Ein bestimmtes konfigurierbares Element, das eine ganze Zahl zwischen 0 und 100 sein muss, verfügt beispielsweise über eine zusätzliche semantische Einschränkung. Solche Einschränkungen werden von der Mergemod.dll und daher sollten Modulautoren darauf vorbereitet sein, alle Zeichenfolgen zu verarbeiten, die den angegebenen Ganzzahlformattyp erfüllen.

 

 



