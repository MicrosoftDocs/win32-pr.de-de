---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960733"
---
# <a name="p-wmi"></a>P (WMI)

[a](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**Leistungs Zählers**
</dt> <dd>

Eine Eigenschaft in einer Leistungsklasse, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet ist und Leistungsdaten speichert.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**Leistungs Objekt**
</dt> <dd>

Ein Objekt in einer Leistungs Bibliothek, in dem Daten in Leistungsindikatoren gespeichert werden. Diese Objekte sind im [*System Monitor*](gloss-s.md) -Hilfsprogramm sichtbar. Beispiele hierfür sind Cache-und logische Datenträger Objekte. Bei der Übertragung in WMI durch den [*ADAP*](gloss-a.md) -Prozess werden die einzelnen Objekte zu zwei WMI-Leistungsklassen. Eine Klasse, die Rohdaten enthält, wird von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet. Die andere Klasse wird von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet und enthält die gleichen Daten, die im System Monitor sichtbar sind, wie vom gekochten Leistungsindikatoren-Anbieter berechnet.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**dauerhafter Consumer**
</dt> <dd>

Ein [*Ereignisconsumer*](gloss-e.md) , dessen Registrierung so lange dauert, bis er explizit abgebrochen wird. Siehe auch [*temporärer Consumer*](gloss-t.md).

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physischer Consumer**
</dt> <dd>

Ein COM-Objekt, das von einem [*Ereignisconsumeranbieter*](gloss-e.md) implementiert wird und eine [*Senke*](gloss-s.md) für den Empfang von Ereignis Benachrichtigungen enthält.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Property**
</dt> <dd>

Ein Name-Wert-Paar, das eine Dateneinheit für eine Klasse beschreibt. Eigenschaftswerte müssen einen gültigen [*Managed Object Format (MOF)*](gloss-m.md) -Datentyp aufweisen. Siehe auch [*Reference-Eigenschaft*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**Eigenschaften Anbieter**
</dt> <dd>

Ein com-Server, der das Abrufen und Ändern von WMI-Eigenschaften unterstützt. Eigenschafts Anbieter implementieren die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -und [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstellen.

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**ab**
</dt> <dd>

Ein com-Server, der mit verwalteten Objekten kommuniziert, um auf Daten und Ereignis Benachrichtigungen wie die Registrierung oder ein SNMP-Gerät zuzugreifen. Anbieter leiten diese Daten zur Integration und Interpretation an die [*CIM-Objekt-Manager*](gloss-c.md) weiter.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**Provider-Methode**
</dt> <dd>

Eine Methode, die von einem WMI- *Anbieter* implementiert wird.

</dd> </dl>

 

 
