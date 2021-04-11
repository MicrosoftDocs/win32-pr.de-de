---
title: Implementierung der IEnumSTATPROPSETSTG-Compound Datei
description: Die Implementierung der Verbund Datei der ienumstatus propsetstg-Schnittstelle wird verwendet, um ein Array von Statuswert-Strukturen aufzuzählen, die statistische Eigenschaften Daten enthalten.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- Ienumstatus propsetstg-STG, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315333"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>Implementierung der IEnumSTATPROPSETSTG-Compound Datei

Die Implementierung der Verbund Datei der [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Schnittstelle wird verwendet, um ein Array von [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Wert-Strukturen aufzuzählen, die statistische Eigenschaften Daten enthalten. Die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Implementierung verwaltet die statistischen Daten und ist einem aktuellen Verbund Datei-Speicher Objekt zugeordnet.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Aufrufen der Methoden von [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) zum Auflisten von [**Status-setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Strukturen, von denen jede Daten zu einem der Eigenschaften Sätze bereitstellt, die dem Verbund Dateispeicher Objekt zugeordnet sind.

## <a name="remarks"></a>Bemerkungen

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**Ienumstatus propsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ruft das nächste oder mehrere [**Status setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Strukturen ab (die Zahl wird durch den *celt* -Parameter angegeben). Die durch einen Aufrufen der Implementierung der Verbund Datei von [**ienumstatus propsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) bereitgestellten " **Status-setstg** "-Elemente befolgen die folgenden Regeln:

-   Wenn [**ienumstatus propsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) nicht die Angabe von "Status-setstg. fmtid" bieten, werden Nullen in dieses Element geschrieben. Dies tritt auf, wenn der Eigenschaften Satz keinen vordefinierten Namen hat (z. b. \\ 005summaryinformation) und kein gültiger Wert ist.
-   Der Satz "documentsummaryinformation" und der benutzerdefinierte Eigenschaften Satz sind "Special", da er möglicherweise zwei Eigenschaften Satz Abschnitte hat. Dieser Eigenschaften Satz wird im Abschnitt [documentsummaryinformation und UserDefined-Eigenschaften Sätze](the-documentsummaryinformation-and-userdefined-property-sets.md)beschrieben. Der zweite Abschnitt wird als User-Defined Eigenschaften bezeichnet. Jeder Abschnitt wird mit einem eindeutigen Format Bezeichner (fmtid) identifiziert. Wenn [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) zum Auflisten von Eigenschafts Sätzen verwendet wird, wird der User-Defined-Eigenschaften Satz nicht aufgelistet.

> [!Note]  
> Wenn Sie immer einen Eigenschaften Satz mithilfe von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)erstellen, dann wird, da für den Speicher Namen eine "Zeichen-GUID" erstellt wird, [**ienumstatus propsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) eine nicht 0 (null), gültige fmtid für den Eigenschaften Satz " \[ Status-setstg. fmtid" zurückgegeben \] .

 

-   Der Status propsetstg. grfFlags reflektiert nicht notwendigerweise, ob der Eigenschaften Satz ANSI ist oder nicht. Wenn propsetflag \_ ANSI festgelegt ist, ist der Eigenschaften Satz definitiv ANSI. Wenn propsetflag \_ ANSI eindeutig ist, kann der Eigenschaften Satz entweder Unicode oder nicht-Unicode sein, weil es nicht möglich ist, zu erkennen, ob es sich um ANSI handelt, ohne es zu öffnen.
-   Der statpropsetstg. grfFlags-Member gibt an, ob der Eigenschaften Satz einfach ist, sodass die Einstellung des nonsimple-Flags propsetflag \_ immer gültig ist.
-   Wenn [**ienumstatupropsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) die Angabe von "Status-setstg. CLSID" nicht bereitstellen kann, werden alle Nullen (CLSID \_ null) festgelegt. In der Implementierung der com-Verbund Datei tritt dieser Fehler auf, wenn der Eigenschaften Satz einfach ist (das nonsimple-Flag propsetflag \_ ist nicht festgelegt) oder nicht einfach ist, aber die CLSID nicht explizit festgelegt wurde. Bei nicht einfachen Eigenschafts Sätzen ist die empfangene CLSID die von der zugrunde liegenden [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)-Klasse erhaltene CLSID.
-   Wenn [**ienumstatus propsetstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) die Zeitfelder \[ **ctime**, **mtime** und **atime** nicht bereitstellen kann \] , wird jede nicht unterstützte Zeit auf Nullen festgelegt. In der Implementierung der com-Verbund Datei ist das Abrufen dieser Werte davon abhängig, dass Sie von der zugrunde liegenden [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Implementierung abgerufen werden.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**Ienumstatus propsetstg:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Überspringt die Anzahl der in *celt* angegebenen Elemente. Gibt "s OK" zurück \_ , wenn die angegebene Anzahl von Elementen übersprungen wird, gibt "false" zurück, \_ Wenn weniger Elemente als angefordert übersprungen werden. In jedem anderen Fall wird der entsprechende Fehler zurückgegeben.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**Ienumstatus propsetstg:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Legt den Cursor auf den Anfang der Enumeration fest. Wenn erfolgreich, wird S OK zurückgegeben; \_ andernfalls wird STG \_ E \_ InvalidHandle zurückgegeben.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**Ienumstatus propsetstg:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Kopiert den aktuellen Enumerationszustand dieses Enumerators.

</dd> </dl>

 

 