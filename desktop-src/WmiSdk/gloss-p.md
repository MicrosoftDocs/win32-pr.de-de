---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230d3dba8be620b0d2d473dbf23960fff79cb7c76abc8a686c47a630605318d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050788"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F G](gloss-f.md) [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) T [U](gloss-t.md) V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**Leistungsindikator**
</dt> <dd>

Eine Eigenschaft in einer Leistungsklasse, die von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet ist, die Leistungsdaten speichert.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**Leistungsobjekt**
</dt> <dd>

Ein Objekt in einer Leistungsbibliothek, das Daten in Leistungsindikatoren speichert. Diese Objekte sind im [*Systemmonitor-Hilfsprogramm*](gloss-s.md) sichtbar. Beispiele hierfür sind Cache- und Logische Datenträgerobjekte. Bei der Übertragung in WMI durch den [*ADAP-Prozess*](gloss-a.md) wird jedes Objekt zu zwei WMI-Leistungsklassen. Eine Klasse, die Rohdaten enthält, wird von [**Win32 \_ PerfRawData ableiten.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) Die andere Klasse wird von [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ableiten und enthält die gleichen Daten, die im Systemmonitor sichtbar sind, wie vom Anbieter des Zählers für Zähler berechnet.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**Permanenter Consumer**
</dt> <dd>

Ein [*Ereignis consumer,*](gloss-e.md) dessen Registrierung so lange dauert, bis sie explizit abgebrochen wird. Siehe auch [*temporärer Consumer.*](gloss-t.md)

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physischer Consumer**
</dt> <dd>

Ein COM-Objekt, das von einem [*Ereignisverbraucheranbieter implementiert wird,*](gloss-e.md) der eine Senke [*zum*](gloss-s.md) Empfangen von Ereignisbenachrichtigungen enthält.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Eigenschaft**
</dt> <dd>

Ein Name-Wert-Paar, das eine Dateneinheit für eine Klasse beschreibt. Eigenschaftswerte müssen einen gültigen [*MANAGED OBJECT FORMAT -Datentyp (MOF)*](gloss-m.md) haben. Siehe auch [*Referenzeigenschaft*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**Eigenschaftenanbieter**
</dt> <dd>

Ein COM-Server, der das Abrufen und Ändern von WMI-Eigenschaften unterstützt. Eigenschaftenanbieter implementieren die [**Schnittstellen IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**IWbemPropertyProvider.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**Anbieter**
</dt> <dd>

Ein COM-Server, der mit verwalteten Objekten kommuniziert, um auf Daten- und Ereignisbenachrichtigungen wie die Registrierung oder ein SNMP-Gerät zu zugreifen. Anbieter geben diese Daten zur Integration [*und Interpretation CIM-Objekt-Manager*](gloss-c.md) An das Unternehmen weiter.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider-Methode**
</dt> <dd>

Eine Methode, die ein *WMI-Anbieter* implementiert.

</dd> </dl>

 

 
