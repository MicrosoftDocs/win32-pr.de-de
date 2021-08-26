---
description: Festlegen von Eigenschaften für Effekte und Übergänge
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Festlegen von Eigenschaften für Effekte und Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1305eb7860b5519b14cfeebc349643c2662db3f133c0bf3424d1d71ccf85753c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904260"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Festlegen von Eigenschaften für Effekte und Übergänge

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Viele [DirectShow Editing Services-Effekte](directshow-editing-services.md) und -Übergänge unterstützen Eigenschaften, die ihr Verhalten steuern. Eine Anwendung kann den Wert einer Eigenschaft mithilfe der [**IPropertySetter-Schnittstelle**](ipropertysetter.md) festlegen. Das zugrunde liegende Effekt- oder Übergangsobjekt muss **IDispatch** zum Festlegen der Eigenschaften unterstützen. Mit Videoeffekten und Übergängen kann die Anwendung einen Bereich von Werten festlegen, die sich im Laufe der Zeit ändern. (Sie können z. B. einen Löschübergang festlegen, um zwischen den Rahmen zu wechseln.) Bei Audioeffekten ist der Wert der -Eigenschaft statisch und kann sich im Laufe der Zeit nicht ändern. Die einzige Ausnahme ist der [Effekt VolumeUmschlag,](volume-envelope-effect.md) der eine dynamische Eigenschaft für die Volumeebene unterstützt.

Führen Sie die folgenden Schritte aus, um eine Eigenschaft festzulegen.

1.  Erstellen Sie eine Instanz des Eigenschaftensetters (CLSID \_ PropertySetter).
2.  Füllen Sie [**die DEXTER \_ PARAM-**](dexter-param.md) und [**DEXTER \_ VALUE-Strukturen**](dexter-value.md) mit den Eigenschaftsdaten. Diese Strukturen werden im Folgenden erläutert.
3.  Übergeben Sie die [**DEXTER \_ PARAM-**](dexter-param.md) und [**DEXTER \_ VALUE-Strukturen**](dexter-value.md) an die [**IPropertySetter::AddProp-Methode.**](ipropertysetter-addprop.md)
4.  Wiederholen Sie die Schritte 2 und 3 für jede Eigenschaft, die Sie festlegen möchten.
5.  Übergeben Sie den [**IPropertySetter-Schnittstellenzeiger**](ipropertysetter.md) an die [**IAMTimelineObj::SetPropertySetter-Methode.**](iamtimelineobj-setpropertysetter.md)

Die [**DEXTER \_ PARAM-Struktur**](dexter-param.md) gibt an, welche Eigenschaft festgelegt wird. Sie enthält die folgenden Member.

-   **Name:** Name der Eigenschaft
-   **dispID:** Reserviert, muss 0 (null) sein
-   **nValues:** Anzahl der Werte

Die DEXTER \_ VALUE-Struktur gibt den Wert einer Eigenschaft zu einem bestimmten Zeitpunkt an. Sie enthält die folgenden Member.

-   **v:** VARIANT-Typ, der einen neuen Wert für die Eigenschaft angibt. Der **vt-Member** dieses VARIANT definiert den Datentyp der Eigenschaft. Weitere Informationen zum **VARIANT-Typ** finden Sie im Windows SDK.
-   **rt**: Die Referenzzeit, zu der die Eigenschaft diesen Wert annimmt, relativ zur Startzeit des Effekts oder Übergangs. Die Startzeit des Effekts oder Übergangs ist relativ zur Startzeit des übergeordneten Objekts.
-   **dwInterp:** Flag, das angibt, wie sich die Eigenschaft vom vorherigen Wert in den neuen Wert ändert. Mit dem DEXTERF \_ JUMP-Flag springt die Eigenschaft sofort zum neuen Wert zum angegebenen Zeitpunkt. Mit dem DEXTERF \_ INTERPOLATE-Flag wird die -Eigenschaft linear aus dem vorherigen Wert interpoliert.

Wenn Sie den **vt-Member** auf VT \_ BSTR festlegen, nimmt der Eigenschaftensetter alle erforderlichen Konvertierungen vor. Schließen Sie für Gleitkommawerte die führende Null vor der Dezimalstelle ein. Beispiel: 0.3, nicht .3.

> [!Note]  
> Anwendungen sollten die Konvertierung von **BSTR-Werten** in numerische Werte vermeiden. Wenn die Eigenschaft über einen numerischen Wert verfügt, ist die Verwendung des entsprechenden numerischen **VARIANT-Typs** möglich.

 

Der Wert einer Eigenschaft kann sich im Laufe der Zeit ändern, sodass die [**IPropertySetter::AddProp-Methode**](ipropertysetter-addprop.md) eine einzelne [**DEXTER \_ PARAM-Struktur**](dexter-param.md) und einen Zeiger auf ein Array von [**DEXTER \_ VALUE-Strukturen**](dexter-value.md) verwendet. Das -Array definiert einen Satz zeitbasierter Werte für die -Eigenschaft. Die Member des Arrays müssen in aufsteigender Zeitreihenfolge sein, und der **nValues-Member** der DEXTER \_ PARAM-Struktur muss der Länge des Arrays entsprechen.

Im folgenden Codebeispiel werden Eigenschaftsdaten für den [SMPTE Wipe-Übergang](smpte-wipe-transition.md) erstellt. Der Zurücksetzungscode wird auf 120 festgelegt, wodurch ein ovales Zurücksetzen erstellt wird. Die Referenzzeit wird auf 0 (null) festgelegt, was den Beginn des Übergangs angibt.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Dynamisches Ändern von Eigenschaften**

Nachdem Sie ein Videobearbeitungsprojekt gerendert haben, können Sie die Eigenschaften eines Effekt- oder Übergangsobjekts ändern, während das Diagramm ausgeführt wird. Dies ist jedoch nur möglich, wenn Sie Eigenschaften für dieses Objekt vor der Anwendung mit dem Namen [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md)festlegen. Wenn dies der Fall ist, können Sie [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) für den Effekt oder Übergang aufrufen, die Eigenschaften löschen oder ändern, und die Änderungen werden dynamisch ausgeführt, während das Diagramm ausgeführt wird. Während der Änderung können visuelle Anomalien auftreten, daher wird dies nur für die Vorschau empfohlen. Ändern Sie die Eigenschaften nicht, während Sie das Projekt in eine Datei schreiben.

Wenn Sie keine Eigenschaften für das Effekt- oder Übergangsobjekt festgelegt haben, bevor Sie **ConnectFrontEnd** aufgerufen haben, können Sie ihr keine Eigenschaften hinzufügen, während das Diagramm ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



