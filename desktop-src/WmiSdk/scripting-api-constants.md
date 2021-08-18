---
description: Die Skripterstellungs-API für WMI enthält Flags, allgemeine Werte und Fehlercodes.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Skripterstellungs-API-Konstanten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84e52c329fc311e7f99a6564ac51f90574308e31fa1eaa90bfb6d0bcdddc69b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130872"
---
# <a name="scripting-api-constants"></a>Skripterstellungs-API-Konstanten

WMI verwendet mehrere Typen von Konstanten im *iflags-Parameter* von Methodenaufrufen in der [Skripterstellungs-API für WMI.](scripting-api-for-wmi.md)

Visual Basic Anwendungen können die Typbibliothek für die Skript-API Wbemdisp.tlb enthalten. Skripts können nicht auf Konstanten in der Typbibliothek zugreifen, es sei denn, sie verwenden die <REFERENCE> Tags oder aus dem <OBJECT> XML-Dateiformat Windows Script Host (WSH), wie unter [Verwenden der WMI-Skripttypbibliothek](using-the-wmi-scripting-type-library.md)beschrieben. Andernfalls muss ein Skript den Wert der Konstante verwenden.

## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Definieren Sie die Sicherheitsauthentifizierungsebenen.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Definieren Sie, wie ein Schreibvorgang in eine Klasse oder eine Instanz ausgeführt wird.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Definieren Sie die gültigen CIM-Typen eines Eigenschaftswerts.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Definieren Sie die Einstellungen für den Objektvergleich und werden von [**SWbemObject.CompareTo \_**](swbemobject-compareto-.md)verwendet.

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Definiert ein Sicherheitsflag, das als Parameter in Aufrufen der [**SWbemLocator.ConnectServer-Methode**](swbemlocator-connectserver.md) verwendet wird, wenn eine Verbindung mit WMI auf einem Remotecomputer fehlschlägt.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Definieren Sie die Fehler, die von der [Skripterstellungs-API für WMI-Aufrufe](scripting-api-for-wmi.md) zurückgegeben werden können.

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Definiert Konstanten, die von [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync,**](swbemservices-execqueryasync.md) [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)und [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)verwendet werden.

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Definieren Sie die Sicherheitsidentitätswechselebenen. Diese Konstanten werden mit [**SWbemSecurity**](swbemsecurity.md)verwendet.

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Definieren Sie die gültigen Objekttextformate, die von [**SWbemObjectEx.GetText \_**](swbemobjectex-gettext-.md)verwendet werden sollen.

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Definieren Sie Berechtigungen. Diese Konstanten werden mit [**SWbemSecurity**](swbemsecurity.md) verwendet, um die für einige Vorgänge erforderlichen Berechtigungen zu gewähren.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Definieren Sie die Tiefe der Enumeration oder Abfrage, die bestimmt, wie viele Objekte von einem Aufruf zurückgegeben werden.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Definiert den Inhalt des generierten Objekttexts und wird von [**SWbemObject.GetObjectText \_**](swbemobject-getobjecttext-.md)verwendet.

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Definiert die Time out-Konstanten. Diese Konstante wird von [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md)verwendet.

</dd> </dl>

## <a name="combining-flags"></a>Kombinieren von Flags

Sie können Flags kombinieren, um mehr als einen Aspekt des API-Aufrufs zu beeinflussen.

Um beispielsweise einen [*semisynchronen*](gloss-s.md) Aufruf zu erstellen, muss der *iFlags-Parameter* in einem [**SWbemServices.Exe\_ cQuery-Aufruf**](swbemservices-execquery.md) zwei Flags enthalten: **WbemFlagReturnImmediately** und **WbemFlagForwardOnly**. Der Wert von **WbemFlagReturnImmediately** ist 16, und der Wert von **WbemFlagForwardOnly** ist 32. Da auf die Konstanten nicht anhand des Namens zugegriffen werden kann, werden die Werte dieser Flags kombiniert, wodurch ein *iFlags-Wert* von 48 erzeugt wird.

Das folgende Skriptbeispiel zeigt den Aufruf.


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

[Skripterstellungs-API für WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



