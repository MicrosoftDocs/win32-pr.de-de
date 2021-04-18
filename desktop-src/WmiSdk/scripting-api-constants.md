---
description: Die Skript-API für WMI enthält Flags, allgemeine Werte und Fehlercodes.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Skript-API-Konstanten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347894"
---
# <a name="scripting-api-constants"></a>Skript-API-Konstanten

WMI verwendet verschiedene Typen von Konstanten im *IFlags* -Parameter von Methoden aufrufen in der [Skript-API für WMI](scripting-api-for-wmi.md).

Visual Basic Anwendungen können die Typbibliothek für die Skript-API, wbemdisp. tlb, enthalten. Skripts können nicht auf Konstanten in der Typbibliothek zugreifen, es sei denn, Sie verwenden die <REFERENCE> <OBJECT> Tags oder aus dem XML-Dateiformat von Windows Script Host (WSH), wie in [Verwenden der WMI-Skriptingtypbibliothek](using-the-wmi-scripting-type-library.md)beschrieben. Andernfalls muss ein Skript den Wert der Konstanten verwenden.

## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Definieren Sie die Sicherheits Authentifizierungs Ebenen.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**Wbemchangeflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Definieren Sie, wie ein Schreibvorgang für eine Klasse oder eine Instanz ausgeführt wird.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**Wbemcimtypeerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Definieren Sie die gültigen CIM-Typen eines Eigenschafts Werts.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**Wbemcomparisonflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Definieren Sie die Einstellungen für den Objektvergleich und werden von der Datei " [**errbemubject. CompareTo \_**](swbemobject-compareto-.md)" verwendet.

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**Wbemconnectoptionsenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Definiert ein sicherheitsflag, das in Aufrufen der Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " als Parameter verwendet wird, wenn eine Verbindung mit WMI auf einem Remote Computer fehlschlägt.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Hiermit werden die Fehler definiert, die von der [Skript-API für WMI](scripting-api-for-wmi.md) -Aufrufe zurückgegeben werden können.

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**Wbemflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Definiert Konstanten, die von [**SWbemServices.Execquery**](swbemservices-execquery.md)verwendet werden [**,SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md), [**Swap Services. SubclassesOf**](swbemservices-subclassesof.md)und [**Swap Services. InstancesOf**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**Wbemimpersonationlevelenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Definieren Sie die Sicherheits Identitätswechsel Ebenen. Diese Konstanten werden mit " [**Swap Security**](swbemsecurity.md)" verwendet.

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**Wbemubjecttextformataufumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Hiermit werden die gültigen Objekt Textformate definiert, die von " [**errbemubjectex. \_ gettext**](swbemobjectex-gettext-.md)" verwendet werden sollen.

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Definieren von Berechtigungen. Diese Konstanten werden mit " [**Swap Security**](swbemsecurity.md) " verwendet, um die Berechtigungen zu erteilen, die für einige Vorgänge erforderlich sind.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**Wbemqueryflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Definieren Sie die Tiefe der Enumeration oder der Abfrage, die bestimmt, wie viele Objekte von einem-Befehl zurückgegeben werden.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**Wbemtextflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Definiert den Inhalt des generierten Objekt Texts und wird von " [**errbemubject. getobjecttext \_**](swbemobject-getobjecttext-.md)" verwendet.

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**Wbemtimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Definiert die Timeout Konstanten. Diese Konstante wird von " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md)" verwendet.

</dd> </dl>

## <a name="combining-flags"></a>Kombinieren von Flags

Sie können Flags kombinieren, um mehr als einen Aspekt des API-Aufrufes zu beeinflussen.

Um z. b. einen [*semisynchronen*](gloss-s.md) -Befehl zu erstellen, muss der *IFlags* -Parameter in einem [**SWbemServices.Exe\_ cquery**](swbemservices-execquery.md) -Befehl zwei Flags enthalten: **wbemFlagReturnImmediately** und **wbemFlagForwardOnly**. Der Wert von **wbemFlagReturnImmediately** ist 16, und der Wert von **wbemFlagForwardOnly** ist 32. Da auf die Konstanten nicht über den Namen zugegriffen werden kann, werden die Werte dieser Flags kombiniert, sodass ein *IFlags* -Wert von 48 erzeugt wird.

Das folgende Skript Beispiel zeigt den-Befehl.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Nicht alle Flags können kombiniert werden, da sich viele gegenseitig ausschließen und zu unvorhersehbaren Ergebnissen führen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skript-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



