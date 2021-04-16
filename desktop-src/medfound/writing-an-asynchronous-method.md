---
description: In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Schreiben einer asynchronen Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348238"
---
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="6ac73-103">Schreiben einer asynchronen Methode</span><span class="sxs-lookup"><span data-stu-id="6ac73-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="6ac73-104">In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ac73-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="6ac73-105">Asynchrone Methoden sind in der Media Foundation Pipeline allgegenwärtig.</span><span class="sxs-lookup"><span data-stu-id="6ac73-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="6ac73-106">Asynchrone Methoden vereinfachen die Verteilung von Arbeit auf mehrere Threads.</span><span class="sxs-lookup"><span data-stu-id="6ac73-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="6ac73-107">Es ist besonders wichtig, e/a-Vorgänge asynchron auszuführen, damit das Lesen aus einer Datei oder einem Netzwerk den Rest der Pipeline nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="6ac73-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="6ac73-108">Wenn Sie eine Medienquelle oder eine Medien Senke schreiben, ist es von entscheidender Bedeutung, asynchrone Vorgänge ordnungsgemäß zu verarbeiten, da sich die Leistung der Komponente auf die gesamte Pipeline auswirkt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="6ac73-109">Media Foundation Transformationen (MFTs) verwenden synchrone Methoden standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="6ac73-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="6ac73-110">Arbeits Warteschlangen für asynchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="6ac73-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="6ac73-111">In Media Foundation gibt es eine enge Beziehung zwischen [asynchronen Rückruf Methoden](asynchronous-callback-methods.md) und [Arbeits Warteschlangen](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="6ac73-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="6ac73-112">Eine Arbeits Warteschlange ist eine Abstraktion zum Verschieben von Arbeit aus dem Thread des Aufrufers in einen Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="6ac73-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="6ac73-113">Gehen Sie folgendermaßen vor, um Arbeit an einer Arbeits Warteschlange auszuführen:</span><span class="sxs-lookup"><span data-stu-id="6ac73-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="6ac73-114">Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6ac73-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="6ac73-115">Rufen Sie [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein *Ergebnis* Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="6ac73-116">Das Ergebnis Objekt macht [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ac73-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="6ac73-117">Das Ergebnis Objekt enthält drei Zeiger:</span><span class="sxs-lookup"><span data-stu-id="6ac73-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="6ac73-118">Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="6ac73-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6ac73-119">Ein optionaler Zeiger auf ein Zustands Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-119">An optional pointer to a state object.</span></span> <span data-ttu-id="6ac73-120">Wenn angegeben, muss das Zustands Objekt **IUnknown** implementieren.</span><span class="sxs-lookup"><span data-stu-id="6ac73-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="6ac73-121">Ein optionaler Zeiger auf ein privates Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-121">An optional pointer to a private object.</span></span> <span data-ttu-id="6ac73-122">Wenn angegeben, muss dieses Objekt auch **IUnknown** implementieren.</span><span class="sxs-lookup"><span data-stu-id="6ac73-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="6ac73-123">Die letzten beiden Zeiger können **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6ac73-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="6ac73-124">Verwenden Sie diese andernfalls zum Speichern von Informationen über den asynchronen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ac73-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="6ac73-125">[**Mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) wird aufgerufen, um das Arbeits Element in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="6ac73-126">Der Arbeits Warteschlangen Thread ruft die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6ac73-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="6ac73-127">Führen Sie die Arbeit innerhalb der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode aus.</span><span class="sxs-lookup"><span data-stu-id="6ac73-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="6ac73-128">Der *pasynkresult* -Parameter dieser Methode ist der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Zeiger aus Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="6ac73-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="6ac73-129">Verwenden Sie diesen Zeiger, um das State-Objekt und das private-Objekt zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="6ac73-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="6ac73-130">Um das State-Objekt abzurufen, nennen Sie [**imfasynkresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="6ac73-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="6ac73-131">Um das private Objekt abzurufen, nennen Sie [**imfasynkresult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="6ac73-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="6ac73-132">Als Alternative können Sie die Schritte 2 und 3 durch Aufrufen der Funktion " [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) " kombinieren.</span><span class="sxs-lookup"><span data-stu-id="6ac73-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="6ac73-133">Intern ruft diese Funktion [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um das Ergebnis Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="6ac73-134">Das folgende Diagramm zeigt die Beziehungen zwischen dem Aufrufer, dem Ergebnis Objekt, dem Zustands Objekt und dem privaten Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![Diagramm, das ein asynchrones Ergebnis Objekt anzeigt](images/workqueues01.png)

<span data-ttu-id="6ac73-136">Das folgende Sequenzdiagramm zeigt, wie ein-Objekt eine Arbeitsaufgabe in die Warteschlange stellt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="6ac73-137">Wenn der Arbeits Warteschlangen Thread [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)aufruft, führt das-Objekt den asynchronen Vorgang in diesem Thread aus.</span><span class="sxs-lookup"><span data-stu-id="6ac73-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![Diagramm, das zeigt, wie ein Objekt in die Warteschlange eines Arbeits](images/workqueues02.png)

<span data-ttu-id="6ac73-139">Beachten Sie, dass [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Thread aufgerufen wird, der sich im Besitz der Arbeits Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="6ac73-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="6ac73-140">Die **Implementierung des** Aufrufs muss Thread sicher sein.</span><span class="sxs-lookup"><span data-stu-id="6ac73-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="6ac73-141">Wenn Sie die Platform Work Queue (**mfasync \_ Callback \_ Queue \_ Standard**) verwenden, ist es außerdem wichtig, dass Sie den Thread nie blockieren, da dadurch die gesamte Media Foundation Pipeline die Verarbeitung von Daten blockieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ac73-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="6ac73-142">Wenn Sie einen Vorgang ausführen müssen, der blockiert wird oder lange dauert, verwenden Sie eine private Arbeits Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ac73-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="6ac73-143">Um eine private Arbeits Warteschlange zu erstellen, rufen Sie [**mfbelegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)auf.</span><span class="sxs-lookup"><span data-stu-id="6ac73-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="6ac73-144">Jede Pipeline Komponente, die e/a-Vorgänge ausführt, sollte aus demselben Grund verhindern, dass e/a-Aufrufe blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="6ac73-145">Die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle stellt eine nützliche Abstraktion für asynchrone Datei-e/a dar.</span><span class="sxs-lookup"><span data-stu-id="6ac73-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="6ac73-146">Implementieren von BEGIN. ../End... Bau</span><span class="sxs-lookup"><span data-stu-id="6ac73-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="6ac73-147">Wie unter [Aufrufen von asynchronen Methoden](calling-asynchronous-methods.md)beschrieben, verwenden asynchrone Methoden in Media Foundation häufig den **Anfang...** / **Ende...** Bau.</span><span class="sxs-lookup"><span data-stu-id="6ac73-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="6ac73-148">In diesem Muster verwendet ein asynchroner Vorgang zwei Methoden mit Signaturen, die den folgenden ähneln:</span><span class="sxs-lookup"><span data-stu-id="6ac73-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="6ac73-149">Damit die Methode wirklich asynchron ist, muss die Implementierung von **BeginX** die tatsächliche Arbeit in einem anderen Thread durchführen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="6ac73-150">An dieser Stelle kommen Arbeits Warteschlangen ins Spiel.</span><span class="sxs-lookup"><span data-stu-id="6ac73-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="6ac73-151">In den folgenden *Schritten ist der* Aufrufer der Code, der **BeginX** und **EndX** aufruft.</span><span class="sxs-lookup"><span data-stu-id="6ac73-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="6ac73-152">Dabei kann es sich um eine Anwendung oder die Media Foundation Pipeline handeln.</span><span class="sxs-lookup"><span data-stu-id="6ac73-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="6ac73-153">Bei der *Komponente* handelt es sich um den Code, der **BeginX** und **EndX** implementiert.</span><span class="sxs-lookup"><span data-stu-id="6ac73-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="6ac73-154">Der Aufrufer ruft **BEGIN...** auf und übergibt einen Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="6ac73-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="6ac73-155">Die Komponente erstellt ein neues asynchrones Ergebnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="6ac73-156">Dieses Objekt speichert die Rückruf Schnittstelle und das Zustands Objekt des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="6ac73-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="6ac73-157">In der Regel speichert Sie auch alle privaten Zustandsinformationen, die die Komponente benötigt, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="6ac73-158">Das Ergebnis Objekt aus diesem Schritt wird im nächsten Diagramm als "Ergebnis 1" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6ac73-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="6ac73-159">Die Komponente erstellt ein zweites Ergebnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-159">The component creates a second result object.</span></span> <span data-ttu-id="6ac73-160">Dieses Ergebnis Objekt speichert zwei Zeiger: das erste Ergebnis Objekt und die Rückruf Schnittstelle des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="6ac73-161">Dieses Ergebnis Objekt wird im nächsten Diagramm als "Ergebnis 2" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6ac73-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="6ac73-162">Die Komponente ruft [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) auf, um eine neue Arbeitsaufgabe in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="6ac73-163">In der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode führt die Komponente die asynchrone Arbeit aus.</span><span class="sxs-lookup"><span data-stu-id="6ac73-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="6ac73-164">Die Komponente ruft [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) auf, um die Rückruf Methode des Aufrufers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="6ac73-165">Der Aufrufer ruft die **EndX** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6ac73-165">The caller calls the **EndX** method.</span></span>

![Diagramm, das zeigt, wie ein Objekt das Begin/End-Muster implementiert](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="6ac73-167">Beispiel für eine asynchrone Methode</span><span class="sxs-lookup"><span data-stu-id="6ac73-167">Asynchronous Method Example</span></span>

<span data-ttu-id="6ac73-168">Um diese Erörterung zu veranschaulichen, verwenden wir ein Beispiel mit einem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6ac73-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="6ac73-169">Stellen Sie sich eine asynchrone Methode zum Berechnen einer Quadratwurzel vor:</span><span class="sxs-lookup"><span data-stu-id="6ac73-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="6ac73-170">Der *x* -Parameter von `BeginSquareRoot` ist der Wert, dessen Quadratwurzel berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6ac73-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="6ac73-171">Die Quadratwurzel wird im *PVal* -Parameter von zurückgegeben `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6ac73-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="6ac73-172">Hier ist die Deklaration einer Klasse, die diese beiden Methoden implementiert:</span><span class="sxs-lookup"><span data-stu-id="6ac73-172">Here is the declaration of a class that implements these two methods:</span></span>


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="6ac73-173">Die `SqrRoot` Klasse implementiert [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , sodass Sie die Quadratwurzel Operation in einer Arbeits Warteschlange platzieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ac73-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="6ac73-174">Die- `DoCalculateSquareRoot` Methode ist die private-Klassenmethode, die die Quadratwurzel berechnet.</span><span class="sxs-lookup"><span data-stu-id="6ac73-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="6ac73-175">Diese Methode wird vom Arbeitswarteschlangen-Thread aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="6ac73-176">Zunächst benötigen wir eine Möglichkeit, den Wert von *x* zu speichern, damit Sie abgerufen werden kann, wenn der Arbeits Warteschlangen Thread aufruft `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="6ac73-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="6ac73-177">Im folgenden finden Sie eine einfache Klasse, in der die Informationen gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="6ac73-177">Here is a simple class that stores the information:</span></span>


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="6ac73-178">Diese Klasse implementiert **IUnknown** , damit Sie in einem Ergebnis Objekt gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ac73-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="6ac73-179">Der folgende Code implementiert die- `BeginSquareRoot` Methode:</span><span class="sxs-lookup"><span data-stu-id="6ac73-179">The following code implements the `BeginSquareRoot` method:</span></span>


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



<span data-ttu-id="6ac73-180">Im Code werden folgende Schritte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="6ac73-180">This code does the following:</span></span>

1.  <span data-ttu-id="6ac73-181">Erstellt eine neue Instanz der- `AsyncOp` Klasse, die den Wert von *x* enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="6ac73-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="6ac73-182">Ruft [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein Ergebnis Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="6ac73-183">Dieses Objekt enthält mehrere Zeiger:</span><span class="sxs-lookup"><span data-stu-id="6ac73-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="6ac73-184">Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="6ac73-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6ac73-185">Ein Zeiger auf das Zustands Objekt des Aufrufers (*pState*).</span><span class="sxs-lookup"><span data-stu-id="6ac73-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="6ac73-186">Ein Zeiger auf das `AsyncOp`-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="6ac73-187">Ruft [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um ein neues Arbeits Element in die Warteschlange zu stellen</span><span class="sxs-lookup"><span data-stu-id="6ac73-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="6ac73-188">Dieser Befehl erstellt implizit ein äußeres Ergebnis Objekt, das die folgenden Zeiger enthält:</span><span class="sxs-lookup"><span data-stu-id="6ac73-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="6ac73-189">Ein Zeiger auf die `SqrRoot` [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ac73-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6ac73-190">Ein Zeiger auf das innere Ergebnis Objekt aus Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="6ac73-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="6ac73-191">Der folgende Code implementiert die- `SqrRoot::Invoke` Methode:</span><span class="sxs-lookup"><span data-stu-id="6ac73-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



<span data-ttu-id="6ac73-192">Diese Methode ruft das innere Ergebnis Objekt und das- `AsyncOp` Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6ac73-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="6ac73-193">Anschließend wird das- `AsyncOp` Objekt an das-Objekt weitergeleitet `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6ac73-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="6ac73-194">Schließlich ruft Sie [**imfasynkresult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) auf, um den Statuscode festzulegen, und [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) , um die Rückruf Methode des Aufrufers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="6ac73-195">Die- `DoCalculateSquareRoot` Methode erfüllt genau das, was Sie erwarten würden:</span><span class="sxs-lookup"><span data-stu-id="6ac73-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="6ac73-196">Wenn die Rückruf Methode des Aufrufers aufgerufen wird, liegt es in der Verantwortung des Aufrufers, die **End...** -Methode aufzurufen – in diesem Fall `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6ac73-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="6ac73-197">Der `EndSquareRoot` gibt an, wie der Aufrufer das Ergebnis des asynchronen Vorgangs abruft, der in diesem Beispiel die berechnete Quadratwurzel ist.</span><span class="sxs-lookup"><span data-stu-id="6ac73-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="6ac73-198">Diese Informationen werden im Ergebnis Objekt gespeichert:</span><span class="sxs-lookup"><span data-stu-id="6ac73-198">This information is stored in the result object:</span></span>


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a><span data-ttu-id="6ac73-199">Vorgangs Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="6ac73-199">Operation Queues</span></span>

<span data-ttu-id="6ac73-200">Bisher wurde angenommen, dass ein asynchroner Vorgang jederzeit ausgeführt werden kann, unabhängig vom aktuellen Zustand des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ac73-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="6ac73-201">Nehmen Sie beispielsweise an, was geschieht, wenn eine Anwendung aufruft, `BeginSquareRoot` während ein früherer Aufruf derselben Methode noch aussteht.</span><span class="sxs-lookup"><span data-stu-id="6ac73-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="6ac73-202">Die- `SqrRoot` Klasse kann die neue Arbeitsaufgabe in die Warteschlange stellen, bevor die vorherige Arbeitsaufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ac73-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="6ac73-203">Arbeits Warteschlangen werden jedoch nicht garantiert, dass Arbeitselemente serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="6ac73-204">Beachten Sie, dass eine Arbeits Warteschlange mehr als einen Thread zum Verteilen von Arbeits Elementen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6ac73-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="6ac73-205">In einer Multithread-Umgebung kann ein Arbeits Element aufgerufen werden, bevor das vorherige abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ac73-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="6ac73-206">Arbeitselemente können sogar außerhalb der Reihenfolge aufgerufen werden, wenn ein Kontextwechsel unmittelbar vor dem Aufrufen des Rückrufs stattfindet.</span><span class="sxs-lookup"><span data-stu-id="6ac73-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="6ac73-207">Aus diesem Grund ist es für das Objekt zuständig, Vorgänge für sich selbst zu serialisieren, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6ac73-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="6ac73-208">Anders ausgedrückt: Wenn das-Objekt erfordert *, dass der* Vorgang *a* abgeschlossen ist, bevor der Vorgang *b* gestartet werden kann, darf das Objekt eine Arbeitsaufgabe nicht in die Warteschlange stellen, bis der Vorgang *a* abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ac73-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="6ac73-209">Ein Objekt kann diese Anforderung erfüllen, indem es eine eigene Warteschlange für ausstehende Vorgänge hat.</span><span class="sxs-lookup"><span data-stu-id="6ac73-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="6ac73-210">Wenn eine asynchrone Methode für das-Objekt aufgerufen wird, stellt das-Objekt die Anforderung in eine eigene Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ac73-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="6ac73-211">Wenn jeder asynchrone Vorgang abgeschlossen ist, ruft das-Objekt die nächste Anforderung aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="6ac73-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="6ac73-212">Das [MPEG1Source](mpeg1source-sample.md) -Beispiel zeigt, wie eine solche Warteschlange implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ac73-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="6ac73-213">Eine einzelne Methode kann mehrere asynchrone Vorgänge umfassen, insbesondere dann, wenn e/a-Aufrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="6ac73-214">Wenn Sie asynchrone Methoden implementieren, sollten Sie sich sorgfältig mit den Serialisierungsanforderungen beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="6ac73-215">Ist es z. b. für das-Objekt zulässig, einen neuen Vorgang zu starten, während eine vorherige e/a-Anforderung noch aussteht?</span><span class="sxs-lookup"><span data-stu-id="6ac73-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="6ac73-216">Wenn der neue Vorgang den internen Zustand des Objekts ändert, was geschieht, wenn eine vorherige e/a-Anforderung abgeschlossen ist und Daten zurückgibt, die möglicherweise veraltet sind?</span><span class="sxs-lookup"><span data-stu-id="6ac73-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="6ac73-217">Ein gutes Zustandsdiagramm kann bei der Identifizierung der gültigen Zustandsübergänge helfen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="6ac73-218">Thread übergreifende und prozessübergreifende Überlegungen</span><span class="sxs-lookup"><span data-stu-id="6ac73-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="6ac73-219">Arbeits Warteschlangen verwenden kein COM-Marshalling zum Mars Hallen von Schnittstellen Zeigern über Thread Grenzen hinweg.</span><span class="sxs-lookup"><span data-stu-id="6ac73-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="6ac73-220">Daher wird auch dann, wenn ein Objekt als Apartment Thread registriert ist oder der Anwendungs Thread ein Single Thread-Apartment (STA) eingegeben hat, [**imfasynccallback-Rückrufe**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) von einem anderen Thread aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ac73-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="6ac73-221">In jedem Fall sollten alle Media Foundation Pipeline Komponenten das "beide" Threading Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="6ac73-222">Einige Schnittstellen in Media Foundation definieren Remote Versionen einiger asynchroner Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="6ac73-223">Wenn eine dieser Methoden über Prozess Grenzen hinweg aufgerufen wird, ruft die Media Foundation Proxy-/Stub-DLL die Remote Version der-Methode auf, die das benutzerdefinierte Marshalling der Methoden Parameter ausführt.</span><span class="sxs-lookup"><span data-stu-id="6ac73-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="6ac73-224">Im Remote Prozess übersetzt der Stub den Rückruf wieder in die lokale Methode des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ac73-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="6ac73-225">Dieser Prozess ist sowohl für die Anwendung als auch für das Remote Objekt transparent.</span><span class="sxs-lookup"><span data-stu-id="6ac73-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="6ac73-226">Diese benutzerdefinierten marshallingmethoden werden primär für Objekte bereitgestellt, die in den geschützten Medien Pfad (PMP) geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6ac73-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="6ac73-227">Weitere Informationen zum PMP finden Sie unter [geschützter Medien Pfad](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="6ac73-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ac73-228">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ac73-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ac73-229">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="6ac73-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="6ac73-230">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="6ac73-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



