---
description: Tragbare Windows-Geräte unterstützen die folgenden Speicher Eigenschaften.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Speicher Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Storage
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 404b45a6fe5193a0550b3ecc11feeae264125110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372318"
---
# <a name="storage-properties"></a>Speichereigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Speicher Eigenschaften.



| Eigenschaft                                   | VarType        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Speicher \_ Kapazität**                 | **VT \_ UI8**    | Die Gesamt Speicherkapazität in Bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **WPD- \_ Speicher \_ Kapazität \_ in \_ Objekten**    | **VT \_ UI8**    | Gibt die Gesamt Speicherkapazität in Objekten an. beispielsweise die verfügbaren Steckplätze auf einer SIM-Karte.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **WPD- \_ Speicher \_ Beschreibung**              | **VT \_ LPWSTR** | Eine lesbare Beschreibung des Speichers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **WPD \_ - \_ Speicher \_ Datei \_ Systemtyp**       | **VT \_ LPWSTR** | Eine Zeichen folgen Beschreibung des vom Speicher verwendeten Dateisystems, z. b. "FAT32", "NTFS", "Configuration Manager-Dateisystem" usw.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_freier Speicherplatz auf WPD-Speicher \_ \_ \_ in \_ Bytes**   | **VT \_ UI8**    | Der verfügbare Speicherplatz in Bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **\_freier Speicherplatz in WPD-Speicher \_ \_ \_ in \_ Objekten** | **VT \_ UI8**    | Die Anzahl zusätzlicher Objekte, die auf das Gerät geschrieben werden können. Wenn ein Gerät beispielsweise nur ein einzelnes Objekt zulässt, wäre dies 0 (null), wenn das Objekt bereits vorhanden ist.                                                                                                                                                                                                                                                                                                                                                          |
| **WPD- \_ Speicher \_ Serien \_ Nummer**           | **VT \_ LPWSTR** | Eine anbieterspezifische Seriennummer für den Speicher.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ Maximale \_ Objekt \_ Größe für WPD-Speicher**        | **VT \_ UI8**    | Gibt die maximale Größe eines einzelnen Objekts in Bytes an, das in diesem Speicher abgelegt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **WPD \_ - \_ Speichertyp**                     | **VT \_ UI4**    | Beschreibt den physischen Typ eines Speichermediums.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **WPD- \_ Speicher \_ Zugriffs \_ Funktion**       | **VT \_ UI4**    | Identifiziert jeglichen Schreibschutz, der sich global auf diesen Speicher auswirkt. Dies hat Vorrang vor dem für einzelne Objekte angegebenen Zugriff. Mögliche Werte sind die in der Datei "portabledevice. h" definierte Enumeration der **WPD- \_ \_ \_ \_ speicherzugriffsfunktionsfunktions** Wenn der **WPD- \_ \_ Speichertyp** z. b. Rom ist (d. h. der **WPD- \_ \_ Speichertyp \_ Fixed \_ Rom** oder der **WPD- \_ \_ Speichertyp Wechsel \_ \_ Rom**), muss der WPD-Speicher **\_ \_ Zugriffs \_** Funktionswert der **WPD- \_ Speicher \_ Zugriffs \_ Funktion \_ \_ \_ ohne \_ Objekt \_ Löschung** schreibgeschützt sein. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




